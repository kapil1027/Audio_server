# Audio_server


|______________________NOTES_____________________|

    1) Details of Database can be changed from the program file. The default databse details are:
    
	mydb = mysql.connector.connect(
	  	host="localhost",
  		user="root",
  		password="",
  		database="audio_test"
		)

    2) The code itself will create the nessary tables required for SQL.

    3) The allowed audio file type can be added on and reduced  by changing the details in program 
       variable named:
			ALLOWED_EXTENSIONS = {'mp3', 'wav'}

######################################################
              Details about Create API:-
######################################################

-URL: http://127.0.0.1:5000/

-Type of request: POST

       Variables of request body:

        1) Song Audio type:
		i) audio_type : defines the type of audio file(Expected input: song, audiobook, podcast)
        	ii) songName : Name of uploaded song
                iii) audio : variable sotring the file to be uploaded. 

	2) Audiobook audio type:
		i) audio_type : defines the type of audio file(Expected input: song, audiobook, podcast)
                ii) bookTitle : audio book title  
		iii) author : author of audio book
		iv) narrator : narrator name of audio book
		v)audio : variable sotring the file to be uploaded.

	3) Podcast audio type:
		i) audio_type : defines the type of audio file(Expected input: song, audiobook, podcast)
		ii) podcastName : Name of podcast
		iii) podcastHost : Host of podcast
		iv) podcastParticipants : participents, comma seperated name's 10 count max
		v) audio : variable sotring the file to be uploaded.

######################################################
               Details about Update API:-
######################################################

-URL: "http://127.0.0.1:5000/<audioFileType>/<audioFileID>"
-Type of request: PUT

     Variables of request body:

	1) Song Audio type:
		i) audio_type : defines the type of audio file(Expected input: song, audiobook, podcast)
        	ii) songName : Name of uploaded song
                iii) audio : variable sotring the file to be uploaded. 

	2) Audiobook audio type:
		i) audio_type : defines the type of audio file(Expected input: song, audiobook, podcast)
                ii) bookTitle : audio book title  
		iii) author : author of audio book
		iv) narrator : narrator name of audio book
		v)audio : variable sotring the file to be uploaded.

	3) Podcast audio type:
		i) audio_type : defines the type of audio file(Expected input: song, audiobook, podcast)
		ii) podcastName : Name of podcast
		iii) podcastHost : Host of podcast
		iv) podcastParticipants : participents
		v) audio : variable sotring the file to be uploaded.

######################################################
               Details about GET API:-
######################################################

	1)Fetch details for specific file:

		URL: http://127.0.0.1:5000/<audioFileType>/<audioFileID>
		Type of request: GET

	1)Fetch details for all file in one catagory :

		URL: http://127.0.0.1:5000/<audioFileType>
		Type of request: GET

######################################################
               Details about delete API:-
######################################################

	To delete details of file from SQL as well as delete the audio file.
		
		URL: http://127.0.0.1:5000/<audioFileType>/<audioFileID>
		Type of request: DELETE

