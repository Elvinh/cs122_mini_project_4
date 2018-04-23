Implemented all the parts and past the test cases.
Tested using Anaconda3 python(3.6) environment on Windows 10

I fixed a bug on mp4_test.py
        Before:
	ancient = NewsStory('', '', '', '', datetime(1987, 10, 15)).replace(tzinfo=pytz.timezone("EST"))
        future = NewsStory('', '', '', '', datetime(2087, 10, 15)).replace(tzinfo=pytz.timezone("EST"))
        
	After:
	future = NewsStory('', '', '', '', datetime(2087, 10, 15).replace(tzinfo=pytz.timezone("EST")))
	ancient = NewsStory('', '', '', '', datetime(1987, 10, 15).replace(tzinfo=pytz.timezone("EST")))