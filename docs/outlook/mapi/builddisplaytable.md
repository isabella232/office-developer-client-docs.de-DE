---
title: BuildDisplayTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BuildDisplayTable
api_type:
- HeaderDef
ms.assetid: 0846415b-6fe1-4504-8620-108af6719015
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b821394f32a938f4878ee93e685aafbeb0786597
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791386"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**Betrifft**: Outlook 
  
Erstellt eine zeigt die Tabelle aus der Eigenschaftendaten-Seite, die in eine oder mehrere [DTPAGE](dtpage.md) Strukturen enthalten sind. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
STDAPI BuildDisplayTable(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpMalloc,
  HINSTANCE hInstance,
  UINT cPages,
  LPDTPAGE lpPage,
  ULONG ulFlags,
  LPMAPITABLE * lppTable,
  LPTABLEDATA * lppTblData
);
```

## <a name="parameters"></a>Parameter

 _lpAllocateBuffer_
  
> [in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, mit der zusätzlichen Arbeitsspeicher zugewiesen werden. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben. 
    
 _lpMalloc_
  
> Nicht verwendete; sollte auf NULL festgelegt werden. 
    
 _hInstance_
  
> [in] Eine Instanz eines MAPI-Objekts aus dem **BuildDisplayTable** Ressourcen abruft. 
    
 _cPages_
  
> [in] Anzahl der [DTPAGE](dtpage.md) Strukturen im Array auf den durch den Parameter _LpPage_ verwiesen. 
    
 _lpPage_
  
> [in] Zeiger auf ein Array von **DTPAGE** -Strukturen, die enthalten Informationen zu den Seiten des Display-Tabelle erstellt werden. 
    
 _ulFlags_
  
> [in] Bitmaske der Kennzeichen. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format. 
    
 _lppTable_
  
> [out] Zeiger auf einen Zeiger auf die Tabelle anzeigen, die die [IMAPITable](imapitableiunknown.md) -Schnittstelle verfügbar macht. 
    
 _lppTblData_
  
> [in, out] Zeiger auf einen Zeiger auf eine Tabelle Datenobjekt Verfügbarmachen der [ITableData](itabledataiunknown.md) -Schnittstelle in der Tabelle, die in der _LppTable_ -Parameter zurückgegeben. Keine Tabelle Datenobjekt gewünscht wird, sollte _LppTblData_ anstatt einen Zeigerwert auf NULL festgelegt werden. 
    
## <a name="return-value"></a>R�ckgabewert

Keine
  
## <a name="remarks"></a>Hinweise

MAPI verwendet, die auf den _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ für die meisten Zuweisung von virtuellem Speicher und zur Freigabe, insbesondere für die Verwendung von Clientanwendungen Speicher beim Aufruf von Schnittstellen, um Funktionen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Alles möglich aus die Ressource lesen ist, einschließlich:
  
- Titel der Seite, die, die _UlbLpszLabel_ Member der [DTBLPAGE](dtblpage.md) -Struktur aus dem Dialogfeldtitel in der Ressource lesen. 
    
- Alle Steuerelement Titel, der, die _UlbLpszLabel_ Mitglieder der anderen Steuerstrukturen Lesen aus dem Steuerelementtext in der Ressource. 
    
 **BuildDisplayTable** überschreibt Suchzeichenfolge übergeben in die Strukturen Eingabesteuerelement mit Informationen über die Ressource, was bedeutet, dass der Aufrufer **BuildDisplayTable** dynamisch Seite oder ein Steuerelement Titel angegeben werden kann. Anrufer, die werden müssen, die **BuildDisplayTable** haben, können das Table-Datenobjekt in _LppTableData_ zurückgeben und ändern Sie Zeilen darin; oder sie können die Anzeige Tabelle stattdessen manuell in einem Table-Datenobjekt erstellen. 
  
Wenn _LppTableData_ nicht auf NULL festgelegt ist, ist der Anbieter verantwortlich für die Freigabe des Tabellenobjekts Daten Beendigung mit der Tabelle anzeigen. 
  

