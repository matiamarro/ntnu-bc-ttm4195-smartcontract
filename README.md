# Wedding smart contract
Proejct from NTNU course Blockchain Technologies and Cryptocurrencies - TTM4195.

Consisting to write a Solidity smart contract (SC) and an nonfungible token (NFT) for a monogamous wedding, with some required functionalities.

### Details
Design a SC with the following functionalities (call functions in a meaningful way):
1. engagement (1 point): two users can register their engagement to the SC. This means that they set a date and time for the wedding, together with all the  necessary information. The SC must check that none of the participants is already wed.
2. participations (1 point): the users send out participations using the blockchain. They must both agree on the list of participants, recorded after each participant has confirmed.
3. revoke engagement (1 point): any of the two parties can call the wedding off at any time prior to the  wedding day.
4. wedding (2 points): during the specified wedding day, both parties must agree on getting married.
5. (for fun, so optional) voting (1 point): if at least half of the confirmed participants vote against the wedding within a certain time-frame, the wedding is declared invalid. This would implement the famous sentence “Speak now or forever hold your peace”.
6. issue wedding certificate (1 point): after a successful wedding, the SC will issue a wedding certificate in form of a NFT (see NFT specifications).
7. authorised accounts (1 point): the SC holds a list of authorised addresses forcertain functionalities (read this as ministers or authorities that are called only in case the NFT function burn is used).


Design a NFT implementing a wedding certificate with the following functionalities
(call the functions in a meaningful way):
- mint (1 point): a wedding certificate is issued in the form of a token. Include all the relevant information. Any large files can be included, but must be stored on external services.
- non-transferable (1 point): wedding certificates should not be transferable to others.
- burn (1 point): implement a 2-out-of-three mechanism to burn a wedding certificate, which must be called by either the two spouses or a spouse together with an
authorised address from the wedding service.


To stimulate an effective and deep thinking on the design, each of the above functionalities will be evaluated on correctness (half the points) and security (half the points). If your design has a trivial security flaw, this will result in 0 points for the security part. Forse example, your implementation should prevent:
- function calls from unauthorised users
- storage of very sensitive information (e.g. an ID of the spouses must be included, and date, but what about addresses, phone numbers, etc.?)
- input of illegal or problematic values that could get the process stuck