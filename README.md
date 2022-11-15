# NFT-using-Moralis

GIT LINK:https://github.com/udumulanaveen/NFT-using-Moralis


how we can create your own nfts utilizing the tools that morales gives you morales offers you a very nice integration with ipfs which is the leading solution for
decentralized storage so we can do this in the fly with only ui and with a little of code so we are going to go to here to sign up to our dap we are going to say that
this naveen and that me that's our user this is our integration with metamask now morals and metamask are working their magic and here we are now that we are signed 
into our dab.

we are able to interact with it these actions were deactivated when we were not logged in and this is because minting is a transaction and we need to have an 
ethereum address that is active to send transactions to the blockchain now we want to choose an nft name but we're going to choose that after we choose the file 
because this is going to be something interesting this is the one that we're going to mint is the powerful.

i think was his name the person that created this one so we're going to mint this one as an nft so we're going to choose it we are going to choose the 
name we are going to call it powerful ivan fingers great stamina likes web3 hits the gym and likes to hike drinks too much coffee this is the 
description and the name of our nft now let's go to minute.
  
so let's do it right now we're going to upload a mint this might take a while because there's a bunch of things behind the scenes and this is one of them we 
need to sign up the transaction we are going to be interacting with a contract right now so we need to send the transaction to the contract and we have the
transaction through which we mended the nft it might take a while for us to be able to see it in our open sea and the transaction was confirmed in my open c
collection we have powerful ivan fingers we have all the descripting data about it so obviously we have the image and we have a great stamina likes guev 3 hits 
the gym and likes to hike drinks too much coffee the details is the 10 nft.


That was meant in this contract and it was done through the rinkevi blockchain so we are in the testnet right now and this is it guys it's a very 
cool app and you can mint your own nfts with it but how does this app work. what we have here is a very simple flask app what we do in a flask app is 
usually we have a random pi that runs our app and then that will trigger everything that we have under this app directory over here we have our index.html.
   
with all the elements that we need for the dapp in this case these are our interaction buttons to interact with our login with metamask for the nft minter we 
need to have the name of the nft date description and the most important field of all which is our file element when we upload this file element we are going to 
be able to of loaded and minted with this button that will trigger our logic once our logic runs we display the result of the transaction that trigger are nft minting 
in our result space.
    
let's go to the logic to check what the logic of this is about for analyzing the logic i want you to remember that an nft is like a deed of property if you go in 
your city to the property registry you will find there that they have electronic records and those electronic records contain metadata about the property.

They did says who is the owner but the description and everything that pertains to identifying that property is metadata what is the address of the house what 
is the cadastral information about the house meaning what is the asset value for tax purposes what are the blueprints and measurements of the property everything 
will be there as metadata for nfts is the same when you mint an nft the main thing that you deal with is linking the token with the metadata the token says who is 
the owner because it has the information about that in the blockchain but the metadata identifies the object there are two ways of dealing with it you either can deal
with that in a centralized fashion which is pretty okay but then you will have a single point of failure or you can do it more in line with what the blockchain 
industry is all about you can do it in a decentralized fashion and if you do it that way you will need to have access to ipfs which is the leading solution for 
having decentralized storage in the blockchain the issue.
    
 with that is that if you deal with ipfs directly it might take a little bit of weight lifting for you to be able to have this functionality ready in your dab if 
 you use morales on the other hand this is going to get very easy i will show you the example here we have the function here that triggers when we have selected 
 our file and we click upload what it does is that it will collect the get element by id of our file component that we have in our html that component captures 
 files in an array so that's the reason we're just going to point here to the element 0 because we only want the first file that is captured by that interaction 
 then with this file that we are capturing from that element of our html.
 
 we are creating a new moralist file object now that we have this moralis file object we are able to save that object in a very easy way either to the morale 
 server that will be a little bit centralized or to ipfs which is decentralized and morale supports both methods we are going to do it here in a decentralized way 
 so we are going to send this command image file save to ipfs and this is a moralist function that is saving this moralist object that we created here to ipfs here 
 in the middle we are just deactivating these elements of our website so no one can click on those elements when the process has already started when we save our 
 image to ipfs we will get two things from morales we are going to get the hash of the file in ipfs which is the method that ipfs uses in order to identify that no 
 single file is duplicated in their network.
 
The url which basically has to be provided by someone that has an ipfs gateway in this case morales gives you both and what we are going to get here is the url 
so this is what we are going to get from morales here now that we have that image url then we are going to create a metadata object that contains everything that 
we are going to store regarding our nft we are getting our element by id here which is our name for the name of our nft we are getting our description which is the 
description of our nft and the image which is going to be represented by the image jury that we are getting from morality in the previous step when we have all the
metadata ready we are just going to do the same thing that we did before we are going to store that in ipfs but we are going to do it storing the json object so 
that's what we are doing here you just have to call this scaffolding.

That i'm setting up here with the json javascript object that you have created here and that will do the trick that will serialize this in order to store it in 
ipfs for you and that's something that morales is also giving you out of the box then we have that numeralist file ready and we just save it to ipfs we get our ipfs
url or jury and then with that we can call our mean token function that mean token is done by interacting with an smart contract.

we are using here this is an erc 721 contract which is the base for nft so one of the popular bases for nfts now returning to our logic for our minting token
function what we are doing is just sending a transaction to this contract that we are describing over here and that transaction has to contain the encoded function 
call so we are getting the api only for the function that we are calling with the parameter and that will be encoded by this functionality that we are creating here 
and then that encoded function goes to the transaction as a transaction parameter and then we just send it to the blockchain when we get the transaction hash back we
know that the transaction is being processed so we can print to the user their transaction id and that means that the nft is minted dab and we can see what we did 
right we connected with metal mask then we gave a name to our nft we describe what were the characteristics that we wanted to describe for this nft choose your file 
then you mint it and then you get this transaction when that is done if you go to open c here is our nft
