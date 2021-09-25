---
title: Visual C++-Erweiterungen (Beispiel)
TOCTitle: Visual C++ Extensions Example
ms:assetid: fe57868f-5707-3c5b-cb93-4121732d67cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250305(v=office.15)
ms:contentKeyID: 48548934
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 91525df4b3aa4f836c74d454235d34035d5c291b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588896"
---
# <a name="visual-c-extensions-example"></a>Visual C++--Erweiterungen (Beispiel)


**Gilt für**: Access 2013, Office 2013

In diesem Programm wird gezeigt, wie Werte aus Feldern abgerufen und in C/C++-Variablen konvertiert werden.

In diesem Beispiel werden auch "intelligente Zeiger" verwendet, die automatisch die COM-spezifischen Details der Aufruf- und Verweiszählung für die **IADORecordBinding-Schnittstelle** verarbeiten.

Ohne intelligente Zeiger würden Sie diesen Code schreiben:

```cpp 
 
IADORecordBinding *picRs = NULL; 
... 
TESTHR(pRs->QueryInterface( 
 __uuidof(IADORecordBinding), (LPVOID*)&picRs)); 
... 
if (picRs) picRs->Release(); 
```

Mit intelligenten Zeigern leiten Sie den IADORecordBindingPtr-Typ von dem Typ mit dieser Anweisung von der IADORecordBinding-Schnittstelle ab:

```cpp 
 
_COM_SMARTPTR_TYPEDEF(IADORecordBinding, __uuidof(IADORecordBinding)); 
```

Außerdem instanziieren Sie den Zeiger folgendermaßen:

```cpp 
 
IADORecordBindingPtr picRs(pRs); 
```

Da die Visual C++-Erweiterungen vom **Recordset** -Objekt implementiert werden, übernimmt der Konstruktor für den intelligenten Zeiger PicRs den \_ RecordsetPtr-Zeiger, pRs . Der Konstruktor ruft QueryInterface mithilfe von pRs auf, um den \_ RecordsetPtr-Zeiger pRs zu suchen. Der Konstruktor ruft QueryInterface mithilfe von pRs auf, um die IADORecordBinding-Schnittstelle zu finden.

```cpp 
 
// Visual C++ Extensions Example 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <stdio.h> 
#include <icrsint.h> 
_COM_SMARTPTR_TYPEDEF(IADORecordBinding, __uuidof(IADORecordBinding)); 
 
inline void TESTHR(HRESULT _hr) { if FAILED(_hr) _com_issue_error(_hr); } 
 
class CCustomRs : public CADORecordBinding 
{ 
BEGIN_ADO_BINDING(CCustomRs) 
 ADO_VARIABLE_LENGTH_ENTRY2(2, adVarChar, m_ch_fname, 
 sizeof(m_ch_fname), m_ul_fnameStatus, false) 
 ADO_VARIABLE_LENGTH_ENTRY2(4, adVarChar, m_ch_lname, 
 sizeof(m_ch_lname), m_ul_lnameStatus, false) 
END_ADO_BINDING() 
public: 
 CHAR m_ch_fname[22]; 
 CHAR m_ch_lname[32]; 
 ULONG m_ul_fnameStatus; 
 ULONG m_ul_lnameStatus; 
}; 
 
void main(void) 
{ 
 ::CoInitialize(NULL); 
 try 
 { 
 _RecordsetPtr pRs("ADODB.Recordset"); 
 CCustomRs rs; 
 IADORecordBindingPtr picRs(pRs); 
 
 pRs->Open("SELECT * FROM Employee ORDER BY lname", 
 "dsn=pubs;uid=sa;pwd=;", 
 adOpenStatic, adLockOptimistic, adCmdText); 
 
 TESTHR(picRs->BindToRecordset(&rs)); 
 
 while (!pRs->EndOfFile) 
 { 
 // Process data in the CCustomRs C++ instance variables. 
 printf("Name = %s %s\n", 
 (rs.m_ul_fnameStatus == adFldOK ? rs.m_ch_fname: "<Error>"), 
 (rs.m_ul_lnameStatus == adFldOK ? rs.m_ch_lname: "<Error>")); 
 
 // Move to the next row of the Recordset. 
 // Fields in the new row will automatically be 
 // placed in the CCustomRs C++ instance variables. 
 
 pRs->MoveNext(); 
 } 
 } 
 catch (_com_error &e ) 
 { 
 printf("Error:\n"); 
 printf("Code = %08lx\n", e.Error()); 
 printf("Meaning = %s\n", e.ErrorMessage()); 
 printf("Source = %s\n", (LPCSTR) e.Source()); 
 printf("Description = %s\n", (LPCSTR) e.Description()); 
 } 
 ::CoUninitialize(); 
} 
```

