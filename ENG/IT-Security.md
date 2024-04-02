# Table of Content
- [Table of Content](#table-of-content)
- [Data Protection](#data-protection)
  - [Art. 32 of the GDPR - Security and Processing](#art-32-of-the-gdpr---security-and-processing)
  - [3 Aspects of IT Security](#3-aspects-of-it-security)
  - [Authentication, Authorization, Authorization](#authentication-authorization-authorization)
  - [ISMS (Information Security Management System)](#isms-information-security-management-system)
- [Protection Needs Analysis](#protection-needs-analysis)
  - [Identification of Data to be Protected](#identification-of-data-to-be-protected)
  - [Summarizing Data into Data Groups](#summarizing-data-into-data-groups)
  - [Determining the Worst Possible Consequences of Loss](#determining-the-worst-possible-consequences-of-loss)
  - [Classification into a Protection Category](#classification-into-a-protection-category)
  - [Violation of Laws, Regulations, and Contracts](#violation-of-laws-regulations-and-contracts)
    - [Data Protection Laws](#data-protection-laws)
    - [Co-Determination Regulations](#co-determination-regulations)
    - [Contracts](#contracts)
- [Symmetric Encryption](#symmetric-encryption)
  - [Methods](#methods)
  - [Advantages](#advantages)
  - [Disadvantages](#disadvantages)
- [Asymmetric Encryption](#asymmetric-encryption)
  - [Advantages](#advantages-1)
  - [Disadvantages](#disadvantages-1)
- [2FA - Two-Factor Authentication](#2fa---two-factor-authentication)
  - [Examples of 2FA](#examples-of-2fa)
  - [Authenticating](#authenticating)
  - [Authenticating](#authenticating-1)
  - [Authorizing](#authorizing)
  - [Types of Authentication](#types-of-authentication)
    - [Knowledge](#knowledge)
      - [Examples of Authentication by Knowledge](#examples-of-authentication-by-knowledge)
    - [Possession](#possession)
      - [Examples of Authentication by Possession](#examples-of-authentication-by-possession)
    - [Physical Characteristics / Biometrics](#physical-characteristics--biometrics)
      - [Examples of Authentication by Biometrics](#examples-of-authentication-by-biometrics)

---
<br>

# Data Protection
- GDPR - General Data Protection Regulation
- BDSG - Federal Data Protection Act

## Art. 32 of the GDPR - Security and Processing
[^1]
1. Pseudonymization and encryption of personal data
2. the ability to ensure the ongoing confidentiality, integrity, availability and resilience of processing systems and services
3. the ability to restore the availability of and access to personal data in a timely manner in the event of a physical or technical incident
4. a process for regularly testing, assessing and evaluating the effectiveness of technical and organizational measures for ensuring the security of processing

In addition, compliance and assessment of these requirements must take into account the risks associated with processing.

## 3 Aspects of IT Security
- Confidentiality
- Integrity
- Availability

## Authentication, Authorization, Authorization
[^2]
- Authentication = Verification of the provided data
- Authorization = When information is correct, the other party grants access

## ISMS (Information Security Management System)
[^3]
The establishment of procedures and rules within an organization aimed at defining, controlling, monitoring, maintaining and continually improving information security.

<br>

# Protection Needs Analysis
[^4] [^5]
Protection needs analysis evaluates the appropriateness of data protection based on the information technology used and the information processed. The value of data and functions is typically many times higher than the value of IT devices themselves. Therefore, appropriate security measures must be derived from the security requirements of IT procedures.

<br>

<a href="https://tetfolio.fu-berlin.de/web/ii_555094:9">
  <img src="https://tetfolio.fu-berlin.de/IMPAL/659400.gif" width="500" title="Structure of a protection needs analysis">
</a>

<br>

The protection need is determined by estimating the worst possible consequences of the loss of __confidentiality__, __integrity__, and __availability__. The assessment must be carried out separately for the following six categories of damage:
- Impairment of the right to informational self-determination
- Impairment of personal integrity
- Impairment of task fulfillment
- Negative external impact
- Financial implications
- Violation of laws, regulations, and contracts

<br>

For each application and the processed information, the potential damages and their categorization into "normal," "high," or "very high" classes are considered. If the result of the protection needs analysis classifies the chosen IT procedure into the "normal" class, the measures of basic IT protection are sufficient. In all other cases, a procedure-specific risk analysis must be carried out.

<br>

__The following steps are applied in the protection needs analysis:__
1. Identification of data to be protected
2. Summarizing data into data groups (optional)
3. Determining the worst possible consequences
4. Classification into a protection category

<br>

## Identification of Data to be Protected
The first step is to identify all data processed or stored within the analyzed IT procedure.
> __Example:__ First name, last name, street, house number, postal code, city, research results, patent application

<br>

## Summarizing Data into Data Groups
Often, multiple individual data can be grouped together based on content. Subsequent steps should then be applied to these data groups rather than the individual data they contain.
>__Example:__  
Contact details 
(first name, last name, street, house number, postal code, city)<br> 
Research results<br> 
Patent application

<br>

## Determining the Worst Possible Consequences of Loss
Each data group is evaluated with regard to the six mentioned categories of damage. For each of the six damage categories, it is considered what consequences the impairment of the protection goals __confidentiality__, __integrity__, and __availability__ would have in the worst case.

<br>

>Example Confidentiality:<br>
__Incident:__ Unauthorized individuals gain knowledge of personnel data.<br>
__Consequences:__ Interaction with colleagues may be impaired.

<br>

>Example Integrity:<br>
__Incident:__ Research data is altered unauthorizedly.<br>
__Consequences:__ There is likely to be a loss of regional reputation.

<br>

>Example Availability:<br>
__Incident:__ Personnel data is unavailable.<br>
__Consequences:__ Delays in salary payments occur.

<br>

## Classification into a Protection Category
The worst consequences determined in the estimation considerations must be classified into the categories in the assessment table.

__Here's an example of classification for the loss of confidentiality in a table:__

<table cellspacing="2" cellpadding="2">
  <tbody>
    <tr>
      <td colspan="1" rowspan="2"><b>Damage Categories</b></td>
      <td colspan="1" rowspan="2">Threat</td>
      <td colspan="3" rowspan="1">Damage Estimation&nbsp;</td>
    </tr>
    <tr>
      <td>normal</td>
      <td>high</td>
      <td>very high</td>
    </tr>
    <tr>
      <td>
        Impairment of the right to informational self-determination
      </td>
      <td>Disclosure of data to unauthorized parties</td>
      <td>X</td>
      <td><br></td>
      <td><br></td>
    </tr>
    <tr>
      <td>Impairment of personal integrity</td>
      <td>Abuse of data…</td>
      <td>X</td>
      <td><br></td>
      <td><br></td>
    </tr>
    <tr>
      <td>Impairment of task fulfillment</td>
      <td>Disclosure of data to unauthorized parties…</td>
      <td>X</td>
      <td><br></td>
      <td><br></td>
    </tr>
    <tr>
      <td>Negative external impact</td>
      <td>Abuse of data…</td>
      <td><br></td>
      <td>X</td>
      <td><br></td>
    </tr>
    <tr>
      <td>Financial implications</td>
      <td>Abuse of data…</td>
      <td>X</td>
      <td><br></td>
      <td><br></td>
    </tr>
    <tr>
      <td colspan="2" rowspan="1">
        <strong>resulting protection needs:</strong>
      </td>
      <td colspan="3" rowspan="1"><strong>high</strong></td>
    </tr>
  </tbody>
</table>

<br>

## Violation of Laws, Regulations, and Contracts
All regulations relevant to the respective IT procedure must be considered here.

<br>

### Data Protection Laws
>__Example:__<br> 
Information Processing Act (IVG)<br>
Federal Data Protection Act (BDSG)<br>
General Data Protection Regulation (GDPR)

<br>

### Co-Determination Regulations
>__Example:__ IT basic service agreement

<br>

### Contracts
>__Example:__ Contract for cooperation with an external company

<br>

# Symmetric Encryption
In Symmetric Encryption, both parties use the same key, which is responsible for both encryption and decryption.

## Methods
- AES
- DES
- Triple-DES
- IDEA
- Blowfish
- QUISCI
- Twofish

These methods are very fast even for large amounts of data.

## Advantages
- Simple key management since only one key is needed for encryption and decryption.
- High speed for encryption and decryption.

## Disadvantages
- Only one key for encryption and decryption, key must not fall into unauthorized hands.
- Key must be transmitted securely.
- Number of keys grows quadratically with the number of participants.

# Asymmetric Encryption
Asymmetric Encryption is also known as Public-Key Encryption. Here, there are not only one but two keys, this so-called key pair consists of a private key and a public key. With the private key, data is decrypted or a digital signature is generated. With the public key, data can be encrypted and generated signatures can be verified for their authenticity. This method is very slow and therefore only suitable for small amounts of data.

## Advantages
- Relatively high security.
- Not as many keys needed as with symmetric encryption methods, thus less effort in keeping the key secret.
- No key distribution problem, as public key is accessible to everyone without issues.
- Possibility of authentication through electronic signatures (digital signatures).

## Disadvantages
- Works very slowly, approximately 10,000 times slower than symmetric encryption.
- Large required key length.
- Problems with multiple recipients of an encrypted message, as the message has to be encrypted separately each time.
- Security risk due to the public key accessible to everyone -> Man in the Middle.

# 2FA - Two-Factor Authentication
[^6]
Two-Factor Authentication, also known as 2FA, refers to the identity verification of a user using a combination of two different and particularly independent components.

## Examples of 2FA
- Bank card + PIN
- Fingerprint
- Access cards
- TAN in online banking

## Authenticating
The general "signing in" to a user's service is called authentication.
The user must authenticate themselves with the service.

## Authenticating
[^7]
Once the user has authenticated and the check has been successfully completed, the service or server can authenticate the user successfully.

## Authorizing
Once the user has been successfully authenticated and authorized, permissions can be distributed, which is called authorization.
The same system can also be applied to buildings or similar.

## Types of Authentication
[^8]
Authentication can be achieved through several methods.

### Knowledge
Characteristics:
- Can be forgotten
- Can be duplicated, distributed, passed on, or betrayed
- Can potentially be guessed

#### Examples of Authentication by Knowledge
- Password
- PIN
- Security question

### Possession
Characteristics:
- Creation of a feature incurs comparatively high costs.
- Management of the possession is insecure and involves effort (must be carried)
- Can be lost
- Can be stolen
- Can be handed over, passed on, duplicated
- Can be replaced

#### Examples of Authentication by Possession
- Chip card
- Magnetic stripe card
- RFID card/chip
- Physical key
- Key codes on a hard drive
- SIM card in the mTAN procedure
- Certificate e.g. in SSL
- TAN
- One Time PIN
- USB stick with password safe

### Physical Characteristics / Biometrics
Characteristics:
- Always carried by individuals
- Cannot be passed on to other individuals
- Requires special equipment for recognition
- Subject to change over time or due to accidents
- Cannot be replaced
- May raise privacy concerns

#### Examples of Authentication by Biometrics
- Fingerprint
- Face recognition
- Typing behavior
- Voice recognition
- Iris recognition (eyes)
- Retinal features (eye background)
- Handwriting (signature)
- Hand geometry (hand scanner)
- Palm vein pattern
- Genetic information (DNA)

[^1]: https://gdpr-info.eu/art-32-gdpr/
[^2]: https://www.protonmail.com/blog/what-is-authentication-authorization-accountability/
[^3]: https://en.wikipedia.org/wiki/Information_security_management_system
[^4]: https://en.wikipedia.org/wiki/IT_baseline_protection#Determination_of_protection_requirements
[^5]: https://tetfolio.fu-berlin.de/web/ii_555094:9
[^6]: https://en.wikipedia.org/wiki/Multi-factor_authentication
[^7]: https://en.wikipedia.org/wiki/Authentication
[^8]: https://en.wikipedia.org/wiki/Authentication#Methods
