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
  
> [in] Zeiger auf eine Schnittstellen-ID (Interface Identifier, IID) für das Tabellendatenobjekt. Der gültige Schnittstellenbezeichner wird IID_IMAPITableData. Das Übergeben von NULL im  _lpInterface-Parameter_ bewirkt auch, dass das im  _lppTableData-Parameter_ zurückgegebene Tabellendatenobjekt in die Standardschnittstelle für ein Tabellendatenobjekt übertragen wird. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die zum Zuordnen von zusätzlichem Arbeitsspeicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freispeichern verwendet werden soll. 
    
 _lpvReserved_
  
> [in] Reserviert. NULL muss sein. 
    
 _ulTableType_
  
> [in] Ein Tabellentyp, der einer Clientanwendung oder einem Dienstanbieter als Teil der [IMAPITable::GetStatus-Rückgabedaten](imapitable-getstatus.md) in den Tabellenansichten zur Verfügung steht. Die folgenden Werte sind möglich: 
    
TBLTYPE_DYNAMIC 
  
> Der Inhalt der Tabelle ist dynamisch und kann sich ändern, wenn sich die zugrunde liegenden Daten ändern. 
    
TBLTYPE_KEYSET 
  
> Die Zeilen in der Tabelle sind fest, aber die Werte in diesen Zeilen sind dynamisch und können sich ändern, wenn sich die zugrunde liegenden Daten ändern. 
    
TBLTYPE_SNAPSHOT 
  
> Die Tabelle ist statisch, und der Inhalt ändert sich nicht, wenn sich die zugrunde liegenden Daten ändern. 
    
 _ulPropTagIndexColumn_
  
> [in] Indexnummer der Spalte, die beim Ändern von Tabellendaten verwendet werden soll. 
    
 _lpSPropTagArrayColumns_
  
> [in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die die eigenschaften angeben, die in der Tabelle erforderlich sind, für die das Objekt Daten enthält. 
    
 _lppTableData_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene Tabellendatenobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Die _Eingabeparameter lpAllocateBuffer,_ _lpAllocateMore_ und _lpFreeBuffer_ verweisen auf die [Funktionen MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer.](mapifreebuffer.md) Eine Clientanwendung, die **CreateTable** aufruft, übergibt Zeiger auf die gerade benannten #A0 . Ein Dienstanbieter übergibt die Zeiger an diese Funktionen, die er beim Initialisierungsaufruf empfangen oder mit einem Aufruf der [IMAPISupport::GetMemAllocRoutines-Methode abgerufen](imapisupport-getmemallocroutines.md) hat. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable : IUnknown](imapitableiunknown.md)

