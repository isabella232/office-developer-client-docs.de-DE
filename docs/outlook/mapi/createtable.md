---
title: CreateTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateTable
api_type:
- HeaderDef
ms.assetid: 106ce3d8-d0bf-4a0e-9a15-dc8988d0eb58
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5d4717dad51e7e6b90da59d285268761eec84d7b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564150"
---
# <a name="createtable"></a>CreateTable

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erstellt Strukturen und Objekt-Handle für ein [ITableData](itabledataiunknown.md) -Objekt, die zum Erstellen des Inhaltsverzeichnisses verwendet werden kann. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
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
  
> [in] Zeiger auf eine Schnittstellenbezeichner (IID) für das Table-Datenobjekt. Der Bezeichner gültige Schnittstelle ist IID_IMAPITableData. Übergeben NULL im _LpInterface_ -Parameter wird auch das Table-Objekt, Daten, die in der _LppTableData_ -Parameter in der standard-Benutzeroberfläche für ein Table-Datenobjekt umgewandelt werden zurückgegeben. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, mit der zusätzlichen Arbeitsspeicher zugewiesen werden. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben. 
    
 _lpvReserved_
  
> [in] Reserviert. NULL muss sein. 
    
 _ulTableType_
  
> [in] Eine Tabellentyp, der als Teil der [IMAPITable::GetStatus](imapitable-getstatus.md) Zurückgeben von Daten in der Tabellenansichten auf eine Clientanwendung oder den Dienstanbieter verfügbar ist. Die folgenden Werte sind möglich: 
    
TBLTYPE_DYNAMIC 
  
> Inhalt der Tabelle sind dynamisch und ändern können, als die zugrunde liegenden Daten geändert. 
    
TBLTYPE_KEYSET 
  
> Die Zeilen in der Tabelle behoben werden, aber die Werte in diesen Zeilen sind dynamisch und ändern können, als die zugrunde liegenden Daten geändert. 
    
TBLTYPE_SNAPSHOT 
  
> Die Tabelle ist statisch und den Inhalt nicht ändern, wenn die zugrunde liegenden Daten geändert. 
    
 _ulPropTagIndexColumn_
  
> [in] Die Indexnummer der Spalte für die Verwendung beim Ändern von Tabellendaten. 
    
 _lpSPropTagArrayColumns_
  
> [in] Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Eigenschaftentags, der angibt, in der Tabelle, für die das Objekt Daten enthält, erforderlichen Eigenschaften enthält. 
    
 _lppTableData_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene Tabelle Datenobjekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Die Eingabeparametern _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ zeigen die [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md) -Funktionen. Eine Clientanwendung Aufrufen **CreateTable** übergibt Zeiger auf die MAPI-Funktionen, die nur mit dem Namen; Ein Dienstanbieter übergibt die Zeiger auf diese Funktionen, die sie in der Initialisierung Anruf empfangen oder mit einem Aufruf der Methode [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) abgerufen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable : IUnknown](imapitableiunknown.md)

