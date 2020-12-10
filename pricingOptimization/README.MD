{\rtf1\ansi\ansicpg1252\cocoartf1561\cocoasubrtf600
{\fonttbl\f0\fnil\fcharset0 HelveticaNeue;}
{\colortbl;\red255\green255\blue255;\red27\green31\blue34;\red255\green255\blue255;\red27\green31\blue34;
}
{\*\expandedcolortbl;;\cssrgb\c14118\c16078\c18039;\cssrgb\c100000\c100000\c100000;\cssrgb\c14118\c16078\c18039;
}
{\*\listtable{\list\listtemplateid1\listhybrid{\listlevel\levelnfc0\levelnfcn0\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{decimal\}.}{\leveltext\leveltemplateid1\'02\'00.;}{\levelnumbers\'01;}\fi-360\li720\lin720 }{\listname ;}\listid1}}
{\*\listoverridetable{\listoverride\listid1\listoverridecount0\ls1}}
\paperw11900\paperh16840\margl1440\margr1440\vieww10800\viewh8400\viewkind0
\deftab720
\pard\pardeftab720\sl600\sa320\partightenfactor0

\f0\b\fs24 \cf2 \cb3 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 ## Pricing \cf4 \cb3 \outl0\strokewidth0 optimization\cf2 \cb1 \outl0\strokewidth0 \strokec2 \
\pard\pardeftab720\sl440\sa320\partightenfactor0
\cf2 \cb3 # Goal: 
\b0 to evaluate whether a pricing test running on the site has been successful. Here, I focus on user segmentation and provide insights about segments who behave differently as well as any other insights you might find.
\b \cb1 \
\cb3 Data Description\
\pard\pardeftab720\sl360\sa320\partightenfactor0

\b0 \cf2 Company XYZ sells a software for $39. Since revenue has been flat for some time, the VP of Product has decided to run a test increasing the price. She hopes that this would increase revenue. In the experiment, 66% of the users have seen the old price ($39), while a random sample of 33% users a higher price ($59).\
The test has been running for some time and the VP of Product is interested in understanding how it went and whether it would make sense to increase the price for all the users. Especially she asked you the following questions:\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sl360\sa320\partightenfactor0
\ls1\ilvl0\cf2 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	1.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Should the company sell its software for $39 or $59?\cb1 \
\ls1\ilvl0\cb3 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	2.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 The VP of Product is interested in having a holistic view into user behavior, especially focusing on actionable insights that might increase conversion rate. What are your main findings looking at the data?\cb1 \
\ls1\ilvl0\cb3 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	3.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 The VP of Product feels that the test has been running for too long and she should have been able to get statistically significant results in a shorter time. Do you agree with her intuition? After how many days would you have stopped the test? Please, explain why.
\b \cb1 \
\pard\pardeftab720\sl440\sa320\partightenfactor0
\cf2 \cb3 Data\
\pard\pardeftab720\sl360\sa320\partightenfactor0

\b0 \cf2 The two tables are:
\b \cb1 \
\pard\pardeftab720\sl360\sa320\partightenfactor0
\cf2 \cb3 "test_results" - data about the test\
\pard\pardeftab720\sl360\sa320\partightenfactor0

\b0 \cf2 Columns:\
user_id : the Id of the user. Can be joined to user_id in user_table\
timestamp : the date and time when the user hit for the first time company XYZ\uc0\u8232 webpage. It is in user local time\
source : marketing channel that led to the user coming to the site. It can be:\uc0\u8232 ads-["google", "facebook", "bing", "yahoo", "other"]. That is, user coming from\u8232 google ads, yahoo ads, etc.\u8232 seo - ["google", "facebook", "bing", "yahoo", "other"]. That is, user coming from google search, yahoo, facebook, etc.\
friend_referral : user coming from a referral link of another user\
direct_traffic: user coming by directly typing the address of the site on the browser\
device : user device. Can be mobile or web\
operative_system : user operative system. Can be: "windows", "linux", "mac" for web, and "android", "iOS" for mobile. "Other" if it is none of the above\
test: whether the user was in the test (i.e. 1 -> higher price) or in control (0 -> old, lower price)\
price : the price the user sees. It should match test\
converted : whether the user converted (i.e. 1 -> bought the software) or not (0 -> left the site without buying it).\
\pard\pardeftab720\sl300\partightenfactor0

\b \cf2 \cb1 \
\pard\pardeftab720\sl360\sa320\partightenfactor0
\cf2 \cb3 "user_table" - Information about the user\
\pard\pardeftab720\sl360\sa320\partightenfactor0

\b0 \cf2 Columns: user_id : the Id of the user. Can be joined to user_id in test_results table\
city : the city where the user is located. Comes from the user ip address\
country : in which country the city is located\
lat : city latitude - should match user city\
long : city longitude - should match user city\
\pard\pardeftab720\sl360\partightenfactor0
\cf2 This challenge has been taken from the book "A collection of Data Science Take-home Challenges" by Giulio Palombo.\
}