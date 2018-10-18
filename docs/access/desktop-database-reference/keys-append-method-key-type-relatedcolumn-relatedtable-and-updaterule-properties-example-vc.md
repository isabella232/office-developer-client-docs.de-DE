---
<span data-ttu-id="242cf-101"><<<<<<< HEAD-Titel: Keys-Methode Append, Schlüsseltyp, RelatedColumn-Eigenschaft (Beispiel) (VC++) TOCTitle: Schlüssel Append-Methode, Schlüsseltyp, RelatedColumn-, RelatedTable- und UpdateRule-Eigenschaft-Beispiel) (VC++) === Titel: Schlüssel Append-Methode Key-Typ, RelatedColumn-Eigenschaft (Beispiel) (VC++) TOCTitle: Schlüssel Append-Methode, Schlüsseltyp, RelatedColumn-, RelatedTable- und UpdateRule-Eigenschaften (VC++-Beispiel)</span><span class="sxs-lookup"><span data-stu-id="242cf-101"><<<<<<< HEAD title: Keys Append Method, Key Type, RelatedColumn Properties Example (VC++) TOCTitle: Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VC++) ======= title: Keys Append Method, Key Type, RelatedColumn properties example (VC++) TOCTitle: Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule properties example (VC++)</span></span>
>>>>>>> <span data-ttu-id="242cf-102">Master Ms:assetid: d0784eb5-94aa-ef62-c26f-3d0980485990 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250041(v=office.15) Ms:contentKeyID: 48547840 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="242cf-102">master ms:assetid: d0784eb5-94aa-ef62-c26f-3d0980485990 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250041(v=office.15) ms:contentKeyID: 48547840 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="242cf-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="242cf-103"><<<<<<< HEAD</span></span>
# <a name="keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vc"></a><span data-ttu-id="242cf-104">Append-Methode (Keys), Key Type-, RelatedColumn-, RelatedTable- und UpdateRule-Eigenschaft (VC++-Beispiel)</span><span class="sxs-lookup"><span data-stu-id="242cf-104">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VC++)</span></span>
=======
# <a name="keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vc"></a><span data-ttu-id="242cf-105">Keys-Methode Append, Schlüsseltyp, RelatedColumn-, RelatedTable- und UpdateRule-Eigenschaften (VC++-Beispiel)</span><span class="sxs-lookup"><span data-stu-id="242cf-105">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule properties example (VC++)</span></span>
>>>>>>> <span data-ttu-id="242cf-106">master</span><span class="sxs-lookup"><span data-stu-id="242cf-106">master</span></span>


<span data-ttu-id="242cf-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="242cf-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="242cf-p101">Im folgenden Code wird das Erstellen eines neuen Fremdschlüssels veranschaulicht. Für das Beispiel wird vorausgesetzt, dass zwei Tabellen (Customers und Orders) vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="242cf-p101">The following code demonstrates how to create a new foreign key. It assumes two tables (Customers and Orders) exist.</span></span>

```cpp 
 
// BeginCreateKeyCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
#import "c:\Program Files\Common Files\system\ado\msado15.dll" 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void CreateKeyX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 CreateKeyX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// CreateKeyX Function // 
// // 
////////////////////////////////////////////////////////// 
void CreateKeyX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _KeyPtr m_pKeyForeign = NULL; 
 _CatalogPtr m_pCatalog = NULL; 
 
 //Define other variables 
 _bstr_t strcnn("Provider='Microsoft.JET.OLEDB.4.0';" 
 "Data source = 'c:\\Program Files\\Microsoft Office\\" 
 "Office\\Samples\\Northwind.mdb';"); 
 try 
 { 
 TESTHR(hr = m_pKeyForeign.CreateInstance(__uuidof(Key))); 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof (Catalog))); 
 m_pCatalog->PutActiveConnection(strcnn); 
 
 // Define the foreign key. 
 m_pKeyForeign->Name = "CustOrder"; 
 m_pKeyForeign->Type = adKeyForeign; 
 m_pKeyForeign->RelatedTable = "Customers"; 
 m_pKeyForeign->Columns->Append("CustomerId",adVarWChar,0); 
 m_pKeyForeign->Columns->GetItem("CustomerId")->RelatedColumn = 
 "CustomerId"; 
 m_pKeyForeign->UpdateRule = adRICascade; 
 
 // To pass as column parameter to Key's Apppend method 
 _variant_t vOptional; 
 vOptional.vt = VT_ERROR; 
 vOptional.scode = DISP_E_PARAMNOTFOUND; 
 
 // Append the foreign key. 
 m_pCatalog->Tables->GetItem("Orders")->Keys-> 
 Append(_variant_t((IDispatch *)m_pKeyForeign), 
 adKeyPrimary,vOptional,L"",L""); 
 printf("Foreign key 'CustOrder' is added.\n"); 
 
 // Delete the key as this is a demonstration. 
 m_pCatalog->Tables->GetItem("Orders")->Keys-> 
 Delete(m_pKeyForeign->Name); 
 printf("Foreign key 'CustOrder' is deleted.\n"); 
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
 cout << "Error occured in include files...."<< endl; 
 } 
} 
// EndCreateKeyCpp 
```

