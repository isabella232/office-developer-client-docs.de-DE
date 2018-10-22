---
<<<<<<< HEAD-Titel: Parameters-Auflistung, Command-Eigenschaft (VC++-Beispiel) TOCTitle: Parameters-Auflistung, Command-Eigenschaft (VC++-Beispiel) === Titel: Parameters-Auflistung, Command-Eigenschaft (VC++-Beispiel) TOCTitle: Parameters-Auflistung, Command-Eigenschaft (VC++-Beispiel)
>>>>>>> Master Ms:assetid: 625a83d5-5b73-f945-7e01-bf412fed0827 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249369(v=office.15) Ms:contentKeyID: 48545237 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="parameters-collection-command-property-example-vc"></a>Parameters-Auflistung, Command-Eigenschaft (VC++-Beispiel)
=======
# <a name="parameters-collection-command-property-example-vc"></a>Parameters-Auflistung, Command-Eigenschaft (VC++-Beispiel)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Im folgenden Codebeispiel wird die Verwendung der [Command](command-property-adox.md)-Eigenschaft mit dem [Command](command-object-ado.md)-Objekt veranschaulicht, um Parameterinformationen für die Prozedur abzurufen.

```cpp 
 
// This sample runs correctly only if procedure 'CustomerById' 
// exists. If the procedure doesn't exist, please use 
// 'ADOXProceduresAppend.cpp' to creat it. 
 
// BeginProcedureParametersCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
#import "c:\Program Files\Common Files\system\ado\msado15.dll" 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void ProcedureParametersX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 ProcedureParametersX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// ProcedureParametersX Function // 
// // 
////////////////////////////////////////////////////////// 
void ProcedureParametersX() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 
 //Define ADODB object pointers. 
 ADODB::_ConnectionPtr m_pCnn = NULL; 
 ADODB::_CommandPtr m_pCommand = NULL; 
 ADODB::_ParameterPtr m_pParameter = NULL; 
 
 try 
 { 
 TESTHR(hr = m_pCnn.CreateInstance(__uuidof(ADODB::Connection))); 
 
 //Open the Connection 
 m_pCnn->Open("Provider='Microsoft.JET.OLEDB.4.0';" 
 "Data Source='c:\\Program Files\\Microsoft Office\\" 
 "Office\\Samples\\Northwind.mdb';","","",NULL); 
 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof(Catalog))); 
 
 //Open the catalog 
 m_pCatalog->PutActiveConnection(_variant_t((IDispatch *)m_pCnn)); 
 
 //Get the command object 
 m_pCommand = m_pCatalog->Procedures->GetItem("CustomerById")-> 
 GetCommand(); 
 
 _variant_t vIndex; 
 
 //Retrieve Parameter information 
 m_pCommand->Parameters->Refresh(); 
 for (long lIndex = 0; lIndex < m_pCommand->Parameters->Count; 
 lIndex ++) 
 { 
 vIndex = lIndex; 
 m_pParameter = m_pCommand->Parameters->GetItem(vIndex); 
 cout << m_pParameter->Name << ":" << m_pParameter->Type << 
 "\n" << endl; 
 } 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 printf("\n\tSource : %s \n\tdescription : %s \n ", 
 (LPCSTR)bstrSource,(LPCSTR)bstrDescription); 
 } 
 
 catch(...) 
 { 
 cout << "Error occured in ProcedureParametersX...."<< endl; 
 } 
} 
// EndProcedureParametersCpp 
```
