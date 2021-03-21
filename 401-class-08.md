# Access Control (ACL)

## Review, Research, and Discussion

1. When is Basic Authorization used vs. Bearer Authorization?

- Basic:
  - is used to ensure correct login information. 
  - it starts by handling encoded information that is passed from the client to the server, that then compares this to data stored that is stored in a database that has been previously encrypted.

- Bearer:
  - another layer of security that grants users access only if the user possess a token


2. What does the JSON Web Token package do?

- creates and verifies a token as a way to grant users access to certain areas of an application

3. What considerations should we make when creating and storing a SECRET?

- since it is an important means of security, a secret should be hard to guess and to not be easily available to the public


## Terminology

- Encryption:
  - translates/hashes data into a different form that is difficult to crack to ensure the security of important data

- Token:
  - piece of data needed to access otherwise restricted areas of an application

- Bearer:
  - person/thing that carries or holds bad news
  - pertaining to programming, refers to a user having a piece of required data which then grants authorization to elements not available to most users

- Secret:
  - a keyword within the app itself that is used toward authentication

- JSON Web Token:
  - a node package that allows us to create and verify 'tokens'

- Authorization Code:
  - temporary code or authorization that exchanges for an access token
  - obtained from authorization route/endpoint

- Access Token:
  - used in token based authentication which allows access to other routes/data that are otherwise restricted

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?

- Tokens tokens tokens! , bearer authorization, and basic authorization

2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

- How the front end encodes data, how to effectively create front ends to handle back end data (we have very little experience with this), the power of tokens

3. What are you most excited about trying to implement or see how it works?

- I will be excited when I can see the picture in a crystal clear view

## References:

- https://digitalguardian.com/blog/what-data-encryption#:~:text=Data%20encryption%20translates%20data%20into,unencrypted%20data%20is%20called%20plaintext.

- https://stackoverflow.com/questions/4448661/what-is-the-exact-definition-of-token
