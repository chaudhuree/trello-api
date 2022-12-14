## documentation for trello

>create trello account get api key token and testing


1-- create trello account and a board
2-- go to [trello main api](https://developer.atlassian.com/cloud/trello/)
3-- trello rest api thakbe oitay dhukte hobe
4-- choose api introduction : https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/
5-- need to generate api key: https://trello.com/power-ups/admin
6-- generate api key and store it:
	Api: 5dd2370eee30445a39f576f1789a8d09
	secret: 24dd221d0cf810e22191abb5650ce36c72ede5bf70a46692531c19dd3a90a821
7-- now generate token: (link will be in the same page right sidebar) https://trello.com/1/authorize?expiration=never&scope=read,write,account&response_type=token&key=5dd2370eee30445a39f576f1789a8d09

8-- generate token and store it
	Token: ATTAf1cc16679160358b22726bbcfc11446470272369ef9d8424bc9b552fc0f145219B19D85E
9-- go back to the starting page of rest api: https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/#:~:text=be%20kept%20secret!-,Your%20First%20API%20Call,-Now%20that%20you

	or

https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/#your-first-api-call

10-- get the base api with full url  :
	 'https://api.trello.com/1/members/me/boards?key={yourKey}&token={yourToken}'

11-- now go to postman
12-- create a new collection ==>trello
13-- add variable:
	baseurl:https: //api.trello.com
	key(api key): 5dd2370eee30445a39f576f1789a8d09
	token: ATTAf1cc16679160358b22726bbcfc11446470272369ef9d8424bc9b552fc0f145219B19D85E

14-- create a get request :
	{{baseurl}}/1/members/me/boards

	--> add key and token in the params

15-- save and get the request


woo hoo its working

>working with board


now to work with the board::
1-- go to the link: https://developer.atlassian.com/cloud/trello/rest/api-group-actions/

	now suppose we want to get a board.so first we have to create a board cz it need
	board id to view it
	to create a board go to: create board:: https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-post

2-- copy the url and also notice the required part.. only name is required
3-- go to postman
4-- create a post request
5-- use the base url and the existing code get from the url
6- put query parameter:: name then key and then token
7-- key and token should be the last one

8-- save and send a request

woo hoo we have a bord now:

9-- copy the board id and save it :  6399cb6440cbfe020bca066d

10-- go to get a board in the documentation:: https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-get

11-- get the method and url then notice the required things(here board id)
12-- go to postman 
13-- create a get request
14-- use the url and the id and the key and token and send

finall we get out board details


>working with list


now create a list:

1-- go to list
2-- create a list:  https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-post
3-- get the url required parameter(name,idBoard-->board er id ta)
4-- must check parameter dewar time a jeno kono space na thake nahole invalid name/idBoard dekhabe
5-- save and send request


boardId: 6399d653a60b34007ea53d17
listId: 6399dc84bebb610539995f92


main link:  [tested all collection](https://documenter.getpostman.com/view/20773865/2s8YzWS1CT)