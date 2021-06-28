## Use-Case 1:
<img style="height: fit-content; width: auto;" src="FRIDA_PensionInformation_OA3_german/resources/Case1_en.png">  
<p>The customer can call the methode ```configureVisibleContracts()``` which returns the visible contracts if it succeeds. <br>
He can also access the pension cockpit of the DRI which then sends a request with a token to the customer portal. Does this process succeeds the visible contracts get
returned to the customer. </p> <br>

<p>The customer also has the option to calculate a selected contract which he can send to the DRI. The DRI then asks for the master data of the 
selected contract from the customer portal with the method ```requestMasterData(selectedContract, token)``` the request contains the selected
contract and a token, if this process succeeds the DRI gets returned the master data and uses that data to calculate the pension amout, which then
gets returned to the customer.<p>

<img src="FRIDA_PensionInformation_OA3_german/resources/Auth_en.png"> 
<p> The authentication also is carried out by the DRI platform, if the customer wants to configure his contracts he can do that on the DRI platform which then
forwards the request to the customer portal which returns the login data to the customer.</p> <br>
<p> The customer can then login into the customer portal with that data, which then returns a redirect and a token to the customer via the DRI platform.</p>

