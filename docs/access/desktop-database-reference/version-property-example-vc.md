---
<<<<<<< HEAD-Titel: Version-Eigenschaft (VC++-Beispiel) TOCTitle: Version-Eigenschaft (VC++-Beispiel) === Titel: Version-Eigenschaft (VC++-Beispiel) TOCTitle: Version-Eigenschaft (VC++-Beispiel)
>>>>>>> Master Ms:assetid: deda3998-52cd-0068-7f8c-e58c71802226 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250130(v=office.15) Ms:contentKeyID: 48548201 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="version-property-example-vc"></a>Version-Eigenschaft (Beispiel) (VC++)
=======
# <a name="version-property-example-vc"></a>Version-Eigenschaft (VC++-Beispiel)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

In diesem Beispiel wird mit der [Version](version-property-ado.md)-Eigenschaft eines [Connection](connection-object-ado.md)-Objekts die aktuelle ADO-Version angezeigt. Außerdem werden verschiedene dynamische Eigenschaften verwendet, um Folgendes anzuzeigen:

  - Aktueller DBMS-Name und DBMS-Version

  - OLE DB-Version

  - Name und Version des Anbieters

  - ODBC-Version

  - Name und Version des ODBC-Treibers

<!-- end list -->

```cpp 
 
// BeginVersionCpp 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void VersionX(void); 
void PrintProviderError(_ConnectionPtr pConnection); 
void PrintComError(_com_error &e); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 VersionX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// VersionX Function // 
// // 
////////////////////////////////////////////////////////// 
void VersionX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define string variables. 
 _bstr_t strCnn("driver={SQL Server};server='MySqlServer';" 
 "user id='MyUserId';password='MyPassword';database='pubs';"); 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _ConnectionPtr pConnection = NULL; 
 
 try 
 { 
 // Open connection. 
 TESTHR(pConnection.CreateInstance(__uuidof(Connection))); 
 pConnection->Open (strCnn, "", "", adConnectUnspecified); 
 
 printf("ADO Version : %s\n\n",(LPCSTR) pConnection->Version); 
 printf("DBMS Name : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("DBMS Name")->Value); 
 printf("DBMS Version : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("DBMS Version")->Value); 
 printf("OLE DB Version : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("OLE DB Version")->Value); 
 printf("Provider Name : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("Provider Name")->Value); 
 printf("Provider Version : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("Provider Version")->Value); 
 printf("Driver Name : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("Driver Name")->Value); 
 printf("Driver Version : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("Driver Version")->Value); 
 printf("Driver ODBC Version : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("Driver ODBC Version")->Value); 
 
 } 
 
 catch (_com_error &e) 
 { 
 // Notify the user of errors if any. 
 PrintProviderError(pConnection); 
 PrintComError(e); 
 } 
 
 if (pConnection) 
 if (pConnection->State == adStateOpen) 
 pConnection->Close(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// PrintProviderError Function // 
// // 
////////////////////////////////////////////////////////// 
void PrintProviderError(_ConnectionPtr pConnection) 
{ 
 // Print Provider Errors from Connection object. 
 // pErr is a record object in the Connection's Error collection. 
 ErrorPtr pErr = NULL; 
 
 if( (pConnection->Errors->Count) > 0) 
 { 
 long nCount = pConnection->Errors->Count; 
 // Collection ranges from 0 to nCount -1. 
 for(long i = 0; i < nCount; i++) 
 { 
 pErr = pConnection->Errors->GetItem(i); 
 printf("Error number: %x\t%s\n", pErr->Number, 
 (LPCSTR) pErr->Description); 
 } 
 } 
} 
 
////////////////////////////////////////////////////////// 
// // 
// PrintComError Function // 
// // 
////////////////////////////////////////////////////////// 
void PrintComError(_com_error &e) 
{ 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 // Print Com errors. 
 printf("Error\n"); 
 printf("\tCode = %08lx\n", e.Error()); 
 printf("\tCode meaning = %s\n", e.ErrorMessage()); 
 printf("\tSource = %s\n", (LPCSTR) bstrSource); 
 printf("\tDescription = %s\n", (LPCSTR) bstrDescription); 
} 
// EndVersionCpp 
```
