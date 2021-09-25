---
title: CreateTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateTable
api_type:
- HeaderDef
ms.assetid: 106ce3d8-d0bf-4a0e-9a15-dc8988d0eb58
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: da2cce7a36c37ee226aa3fc1d49cea84b19d741c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605083"
---
# <a name="createtable"></a>CreateTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt Strukturen und ein Objekthandle für ein [ITableData-Objekt,](itabledataiunknown.md) das zum Erstellen von Tabelleninhalten verwendet werden kann. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE CreateTable(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  ULONG ulTableType,
  ULONG ulPropTagIndexColumn,
  LPSPropTagArray lpSPropTagArrayColumns,
  LPTABLEDATA FAR * lppTableData
);
```

## <a name="parameters"></a>Parameter

 _lpInterface_
  
> [in] Zeiger auf einen Schnittstellenbezeichner (Interface Identifier, IID) für das Tabellendatenobjekt. Der gültige Schnittstellenbezeichner ist IID_IMAPITableData. Wird NULL im  _LpInterface-Parameter_ übergeben, wird auch das im  _Parameter lppTableData_ zurückgegebene Tabellendatenobjekt in die Standardschnittstelle für ein Tabellendatenobjekt umgewandelt. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die verwendet werden soll, um zusätzlichen Speicher zuzuweisen. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freigeben von Arbeitsspeicher verwendet werden soll. 
    
 _lpvReserved_
  
> [in] Reserviert. NULL muss sein. 
    
 _ulTableType_
  
> [in] Ein Tabellentyp, der einer Clientanwendung oder einem Dienstanbieter als Teil der [IMAPITable::GetStatus](imapitable-getstatus.md) zur Verfügung steht, gibt Daten in den Tabellenansichten zurück. Die folgenden Werte sind möglich: 
    
TBLTYPE_DYNAMIC 
  
> Der Inhalt der Tabelle ist dynamisch und kann sich ändern, wenn sich die zugrunde liegenden Daten ändern. 
    
TBLTYPE_KEYSET 
  
> Die Zeilen in der Tabelle sind behoben, aber die Werte in diesen Zeilen sind dynamisch und können sich ändern, wenn sich die zugrunde liegenden Daten ändern. 
    
TBLTYPE_SNAPSHOT 
  
> Die Tabelle ist statisch, und der Inhalt ändert sich nicht, wenn sich die zugrunde liegenden Daten ändern. 
    
 _ulPropTagIndexColumn_
  
> [in] Indexnummer der Spalte, die beim Ändern von Tabellendaten verwendet werden soll. 
    
 _lpSPropTagArrayColumns_
  
> [in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die die in der Tabelle erforderlichen Eigenschaften angeben, für die das Objekt Daten enthält. 
    
 _lppTableData_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene Tabellendatenobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Eingabeparameter _lpAllocateBuffer,_ _lpAllocateMore_ und _lpFreeBuffer_ verweisen jeweils auf die Funktionen [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer.](mapifreebuffer.md) Eine Clientanwendung, die **CreateTable aufruft,** übergibt Zeiger an die mapi-Funktionen, die gerade benannt wurden. Ein Dienstanbieter übergibt die Zeiger an diese Funktionen, die er in seinem Initialisierungsaufruf empfangen oder mit einem Aufruf der [IMAPISupport::GetMemAllocRoutines-Methode](imapisupport-getmemallocroutines.md) abgerufen hat. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable : IUnknown](imapitableiunknown.md)

