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
ms.openlocfilehash: e8c399569e68b8cb55d803733ed93105ea0be799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435012"
---
# <a name="createtable"></a>CreateTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt Strukturen und ein Objekthandle für ein [ITableData](itabledataiunknown.md) -Objekt, das zum Erstellen von Tabelleninhalten verwendet werden kann. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> in Zeiger auf einen Schnittstellenbezeichner (IID) für das Tabellendaten Objekt. Der gültige Schnittstellenbezeichner ist IID_IMAPITableData. Das übergeben von NULL im _lpInterface_ -Parameter bewirkt außerdem, dass das im _lppTableData_ -Parameter zurückgegebene Tabellendaten Objekt in die Standardschnittstelle für ein Tabellendaten Objekt umgewandelt wird. 
    
 _lpAllocateBuffer_
  
> in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die zum Zuweisen von zusätzlichem Arbeitsspeicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben. 
    
 _lpvReserved_
  
> [in] Reserviert. NULL muss sein. 
    
 _ulTableType_
  
> in Ein Tabellentyp, der für eine Clientanwendung oder einen Dienstanbieter als Teil der [IMAPITable:: GetStatus](imapitable-getstatus.md) -Daten in Tabellen Ansichten zur Verfügung steht. Die folgenden Werte sind möglich: 
    
TBLTYPE_DYNAMIC 
  
> Der Inhalt der Tabelle ist dynamisch und kann geändert werden, wenn die zugrunde liegenden Daten geändert werden. 
    
TBLTYPE_KEYSET 
  
> Die Zeilen in der Tabelle sind festgelegt, aber die Werte in diesen Zeilen sind dynamisch und können geändert werden, wenn die zugrunde liegenden Daten geändert werden. 
    
TBLTYPE_SNAPSHOT 
  
> Die Tabelle ist statisch, und der Inhalt ändert sich nicht, wenn sich die zugrunde liegenden Daten ändern. 
    
 _ulPropTagIndexColumn_
  
> in Die Index Nummer der Spalte, die beim Ändern von Tabellendaten verwendet werden soll. 
    
 _lpSPropTagArrayColumns_
  
> in Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags angibt, die die Eigenschaften enthalten, die in der Tabelle erforderlich sind, für die das Objektdaten enthält. 
    
 _lppTableData_
  
> Out Zeiger auf einen Zeiger auf das zurückgegebene Tabellendaten Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Die _lpAllocateBuffer_-, _LpAllocateMore_-und _lpFreeBuffer_ -Eingabeparameter zeigen auf die [MAPIAllocateBuffer](mapiallocatebuffer.md)-, [MAPIAllocateMore](mapiallocatemore.md)-und [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktionen. Eine Clientanwendung, **** die createable aufruft, übergibt Zeiger auf die soeben benannten MAPI-Funktionen. ein Dienstanbieter übergibt die Zeiger an diese Funktionen, die er bei seinem Initialisierungsaufruf erhalten hat oder die mit einem Aufruf der [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) -Methode abgerufen wurde. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable : IUnknown](imapitableiunknown.md)

