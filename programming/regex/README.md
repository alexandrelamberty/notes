# Regex

::>^(._)$ # Add begin/end space to string=::> $1
::>www\.([a-z0-9]_)(-[a-z0-9]+)?(\.[a-z]+)?[ ]+ # Remove URL=
::>([a-z0-9]_)(-[a-z0-9]+)?\.(com|net|org)[ ]+ # Remove URL=
::>\(._\) # Remove content in brakets=
::>[-_.,()\[\]&+] # Replace special chars by spaces=
::>(cd|dvd|xvid|divx)[0-9]{1,3} # Remove disk tag=
::>\s([1-2][0-9]{3})\s # Remove year=
::> bluray._=
::> hddvd._=
::> dvd._=
::> bdrip._=
::> brrip._=
::> webrip._=
::> divx._=
::> xvid._=
::> x264._=
::> h264._=
hd =
720p =
1080p =
mp3 =
aac =
ac3 =
dts =
multi =
vost =
vo =
subforced =
unrated =
limited =
extended =
repack =
truefrench =
vff =
vfq =
french =
edition =
director's =
director =
cut =
remastered =
proper =
vostfr =
vost =
fr =
1cd =
stv =

::>(?-i)([a-z])([A-Z]) # Insert space between lower/UPPER char=::>$1 $2
::>(^|\S)([ ]{2,})($|\S) # Replace multi spaces by 1 space=::>$1 $3
::>^([ ]*)(\S.*\S)([ ]*)$ # Remove begin/end spaces from string=::>$2

Season Episode 3digit: SxE (MATCH)
(?<!\\p{Alnum})(\\d)(\\d{2})(?!\\p{Alnum})

Clear punctuation, spacing. Lead "The" or "A" (REPLACE)
(^(?i)(The|A)\\b)|[\\p{Punct}\\p{Space}]+

(^(?i)(The|A)\b)|[{\s}{\-}{\:}]|\((19|20)\d{2}\)

Year 19xx or 20xx (MATCH)
(?:19|20)\\d{2}

Year generic  
\\b\\d{4}\\b

Reduce name strict (MATCH)
^(.+)[\\[\\(](<(?:19|20)\d{2}>)[\\]\\)]

Reduce name non-strict
^(.+?)((?:19|20)\\d{2})

IMDB id
(?<=tt)\\d{7}

thetvdb id patterns like http://www.thetvdb.com/?tab=series&id=78874&lid=14
SPLIT URL
[\\s\"<>|]+
CHECK ID
(?<=(^|\\W)id=)\\d+

// Name till year
^(.+?)((?:19|20)\d{2})

^(.+)[\[\(](<(?:19|20)\d{2}>)[\]\)]

^(.+)[\(\[\.\-](<(?:19|20)\d{2}>)[\-\.\]\)]

// Vérifier date avec []
((?:19|20)\d{2})

/////////////////////////////////////////////////////

The.Hobbit-The.Desolation.of.Smaug.(2013).DVDScr.XVID.AC3.Hive-CM8.avi
Elysium.2013.[1080p].BluRay.x264.YIFY.mp4
Elysium.2013.1080p.BluRay.x264.YIFY.www.torrentfreak.com.mp4
The.Family.2013.720p.BluRay.x264.YIFY.mp4
Don Jon [2013] HDRip XViD[AC3]juggs[ETRG].avi
Death Race 2000 1975

// --->

1. Extract Movie name and year: "A-Z-1/2-0-9-A-Z-0-9" -> "A-Z-1/2-0-9"
2. Clean ponctuation: "." -> " "
3. Make space around: "-" -> " - "
4.

^(.+?) ((?:19|20)\d{2}) | (?:HDTV|BluRay|DVDScr|\w{2,3}rip) | (?:x264) | (?:\d{3,4}p) | (?:AC\d)
