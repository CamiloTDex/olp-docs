# Core Services in OLP
Note: Not all core services are built. 

## CS1: BUSINESS IDENTITY VERIFICATION SERVICE
### Objectives of this Service
The objective of this service is to provide the network participants assurance that they have enough information about the other party. Also, provide the participants the framework to sign their documents using blockchain compatible identity during P2P transaction and while interacting with the underlying blockchain and other compatible protocols such as ITN, CBAN, openIDL etc.  

### Business Identity 
Any entity that interacts with another entity must be able to present verifiable credentials that they are legal entities within a certain jurisdiction. All verifiable DID constructs assume that the identity provider such as a government entity issues its own DID on the blockchain so that a verifier can validate that the issuer has indeed provided the identity to the holder.  In this case, we assume that FMCSA or any other government entity doesn’t have a mechanism to sign the claims on the blockchain. Hence, this core service assumes the responsibility of Identity Verification Service. The workflow to create and verify identity is as following:

### Entity creates a blockchain ID/DID
It links a public key, called an “ID Key,” to the blockchain ID and uses the corresponding private key to sign and decrypt messages linked to the blockchain ID. Identity Verification Service signs tokens indicating that the entity who controls the blockchain ID has provided proof of a valid off chain documents (e.g., USDOT #, insurance with adequate coverage etc.). Link these tokens to the blockchain ID. 
The Entity A needs to automatically verify if Entity B, C, D exists, it will simply query the tokens corresponding to their public keys. If Entity A wants to book a shipment with an Entity B, then they can open a secured channel.  
In the US, means carriers and brokers must have Motor Carrier (MC) and Employee Identification Number (EIN.) Shippers should have EINs. Company’s operating authorities have time limits and needs to be renewed by the user and is incumbent upon the user to do so. Their authorities may be revoked due to legal and safety violations. The ID verification service has to monitor the operating status of the companies and update token states. 

### Shipment Identity
Each shipment is assigned an unique identification by the broker and tied (one to one relationship) to a bill of lading, invoice, consignee and shipper (company users), payment, driver, and vehicle. The carrier that moved the shipment may also assign its own unique identification. However, in order to ensure that the shipment that has been broadcasted to the network and to relay that the shipment is not available, each booked shipment must have a DID that is linked with the user. The shipment ID can be the hash of documents during the workflow.  

### Identity Relationships
It is important that all three key participants engaged in booking and moving a shipment maintain the same shipment ID in their off chain storage. They can however, augment that ID with internal vanity IDs.  

## CS2: BOOKING A FULL TRUCKLOAD SHIPMENT
### Objectives of this Service
Provide the network participants a standardized smart contract to book and confirm a FULL TRUCKLOAD shipment for pickup and delivery. In order to execute the smart contract, it requires information about broker and the carrier, shipment details, payment terms, origin/destination etc. However, the transaction that is distributed over the OLP network does not include the details of the shipment. This prevents the rest of the network from discovering details of the shipment. 
### Shipment Transactions
Shipment originators sign and submit booked shipment transactions, but it has to be also signed by the carrier to prevent the originators from adding fake shipment transactions. The transaction should also have a DID of the shipment. Each transaction will have the following attributes:
Originator address — Account address of the sender of the transaction or shipment originator.
Originator public key — The public key that corresponds to the private key used to sign the transaction.
Carrier address - 
Carrier public key - 
Gas price and maximum gas amount — The maximum units of gas the transaction is allowed to consume. For now, both originator and carrier will be responsible for the gas fee.
Expiration time — The time after which the transaction is invalid.
Anything else? - invoice ID? 

## CS3: BOOKING A DRAYAGE  SHIPMENT
### Objectives of this Service
Provide the network participants a standardized smart contract to book and confirm a DRAYAGE shipment for pickup and delivery. In order to execute the smart contract, it requires information about broker and the carrier, shipment details, payment terms, origin/destination etc. However, the transaction that is distributed over the OLP network does not include the details of the shipment. This prevents the rest of the network from discovering details of the shipment. 

## CS4: DECENTRALIZED CONSENSUS SERVICE
### Objectives of this Service
Provide automated consensus of transactions - 1) provide proof of existence of shipment transactions, 2) provide an infrastructure for the participants to deploy shipment smart contracts, 3) deploy core services in smart contracts,  4) anchor with more stable main nets such as Bitcoin, Ethereum. 
We have deployed the test net on Ethereum Rinkeby possibly moving to a separate side chain with validator nodes when the network has enough shipments to justify using a separate infrastructure. Also, running a sustainable POA network comes with several technical and legal challenges that are non-trivial.  

### Participating Nodes
Nodes are instances of servers running onsite or in cloud as a VM of the participants. In the initial stage, dexFreight Inc. will run those nodes. As the network scales, the participants will operate those nodes themselves or request dexFreight to operate nodes on their behalf.  We also anticipate the shipment workflow and the validator node can run off of the same computer or different devices. 

## CS5: SECURED P2P WORKFLOW CHANNELS
### Objectives of this Service
It is the intent of this protocol to allow as a viable alternative P2P negotiation and communication (full workflow) between the business entities without a need for centralized applications. Core services then provides a root of trust for identity, reputation, and tamper evident ledger of mutual transactions. For these parties to communicate with each other in a true P2P environment and be able to use the core services, mutual negotiations and transactions need to happen using a secured and dedicated channel. 

### Creating a Secured Channel
The basic mechanics is that a Business Entity A sends a message signed with one of its published signing keys to Entity B based on one of the service endpoints in the OLP Identity Document. The message contains its published identifier and a secret, such as a nonce or session key encrypted by the published signing key of Entity B. A secure channel is established once Entity A sends a signed acknowledgement message containing its published identifier and the secret encrypted to the public signing key of Entity B. In order to ensure forward secrecy, we recommend that upon initial channel establishment, a long-term secret is exchanged. This secret will be then used to derive a new session key for each subsequent secure session. This ensures that even if one session is compromised, previous and future sessions are not. 

The P2P channel is used to perform price and service negotiations between the participants. The negotiation must occur off chain in a P2P environment and no information is entered into the ledger. 

### Shipment Booking  Upon the Establishment 
Once the negotiation is complete, the workflow of signing contracts, exchanging the proof of pick up and delivery all happen in the P2P environment however both parties agreed upon FTL or DRAYAGE smart contracts

## CS6: SHIPMENT VERIFICATION SERVICE
### Objectives of this Service
Provide the network participants proof of the existence of a shipment. This facilitates other use cases such as tokenization of invoices, dispute settlement, insurance, reputation etc.  

### Obtain Proof of Shipments and Provenance
The proof of shipment should respond to multiple request types. 
The requester may already have a shipment ID and wants to verify if the ID exists in the blockchain. 
The requester may request attributes (available on chain) of a given shipment ID. The requester may request additional off chain attributes of a given shipment ID. This may require a message to be sent to the shipment ID’s originator, which may or may not respond with additional attributes about the shipment. 
The requester may request provenance of the shipment ID including carrier, broker, date of pick up, date of delivery etc. about the shipment. 
The core service cannot guarantee that a shipment was indeed picked up and delivered. This is because telematics devices that track the trucks do not digitally sign transactions on a public ledger. At this point, the confirmation originates from the shipment originator and carrier’s nodes. 

### Confidentiality of Shipment Details
Shipment details such as (origin, destination, conveyance type, cargo type etc.) are confidential details known only to the parties involved in the workflow. Third parties such as insurance (because of claims) and banks (to assess risks) may be provided with details by one of more involved parties without requiring consent from other parties in the workflow. Such confidential data is passed around in the P2P environment and not revealed in the ledger. Access and transfer of confidential data between two parties is out of scope of this protocol. However, the proof of existence of the shipment is anchored in the ledger. 

### Proof of Existence of Shipments
At this point, delivery of the required assurance that a shipment has been processed can be achieved by the network participants member by accessing a node and its transaction history. 



{Figure 18}

### Shipment Addition and Cancellation
A shipment transaction is created right after both parties sign a carrier-broker agreement by submitting it via a smart contract. The transaction must be added to the queue by the shipment originator or a delegated entity (e.g., broker’s TMS, market curator.) 
In the real world, after both parties have signed an agreement, the shipment may be canceled by the shipper or the broker or the carrier. The cancel event may happen before or after the transaction has been submitted for inclusion in the blockchain. When this happens, the shipment originator via a smart contract must submit a transaction that indicates that the previously submitted transaction with a specific ID is invalid. The token associated with the shipment will be locked using the signature of both parties. 

### Prevention of Fluffy Shipments
Since shipments are signed by both parties (broker and carrier, shipper and carrier), these two parties colluding to add fake shipments is low, however possible. Second deterrent is transaction fees to be submitted by both parties. However, this will occur once we have a token structure deployed on the main net.  

## CS7: ON CHAIN REPUTATION SERVICE
### Objectives of this Service
Provide unbiased, transparent, and objective reputation of the network participants, especially the ones involved in processing shipments - 1) provide access to regulatory and security reputation information, 2) provide access to quantifiable performance related reputation. This also allows businesses to programmatically discover other businesses.  At this point, reputation pertains only to companies and not their assets and employees (e.g., drivers). 

The intent of the protocol is to provide a virtual registry of companies with regards to their  legal “status”. It is not up to the protocol to suggest/endorse companies based on their reputation. The protocol does not take upon legal burdens that come with doing so. It is incumbent upon the companies to decide whether or not to transact with the companies given the information provided by the core services. The same principle applies for all types of reputation services provided by the core service. 

### Types of Reputation 
Reputation tied to government regulations - in the US (status of authority, insurance status, tax status), driver’s license, EIN status. 
Reputation tied to performance - on time pickup and delivery, on time payment.

### Regulatory Verification Oracles
This service allows companies to verify various regulatory and legal standings of companies they want to transact with. In many cases, a company want to do businesses with another company simply needs to check whether or not a company has a proper authority (input = MC or USDOT#, output = yes/no.) or whether the company’s registration is in a good standing or not. This allows workflow automation to be seamless without requiring human intervention. The service allows the requesting company to be assured that the output is the same as in the original government source. 

### Performance Reputation on Smart Contracts
The shipment originators and transporters submit, approve, and digitally sign on-time pick up and delivery information about shipments as well as on time payment without disclosing the details of such information. Minimum data needed are shipment ID, binary “yes or no” for on-time pick up, on-time delivery, on-time payment. Added with an amount of delay if the answer was “no.”  The information can be unilaterally submitted, but can be disputed by the other party involved in the transaction.
The intent of the performance reputation is not only to provide a global registry of performance of companies processing shipments but also a service that is natively owned and controlled by the network participants.

