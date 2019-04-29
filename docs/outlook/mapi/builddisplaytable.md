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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8c5e6078be05ff846b7737ff53e9a6338fcb2141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431596"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine Anzeigetabelle aus den Eigenschaftenseiten Daten, die in einer oder mehreren [DTPAGE](dtpage.md) -Strukturen enthalten sind. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
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
  
> in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die zum Zuweisen von zusätzlichem Arbeitsspeicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben. 
    
 _lpMalloc_
  
> Nicht verwendete sollte auf NULL festgelegt werden. 
    
 _hInstance_
  
> in Eine Instanz eines MAPI-Objekts, aus dem **BuildDisplayTable** Ressourcen abruft. 
    
 _cPages_
  
> in Die Anzahl der [DTPAGE](dtpage.md) -Strukturen im Array, auf die durch den _lpPage_ -Parameter verwiesen wird. 
    
 _lpPage_
  
> in Zeiger auf ein Array von **DTPAGE** -Strukturen, die Informationen zu den darzustellenden Tabellenseiten enthalten. 
    
 _ulFlags_
  
> in Bitmaske von Flags. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format. 
    
 _lppTable_
  
> Out Zeiger auf einen Zeiger auf die Anzeigetabelle, die die [IMAPITable](imapitableiunknown.md) -Schnittstelle verfügbar macht. 
    
 _lppTblData_
  
> [in, out] Zeiger auf einen Zeiger auf ein Tabellendaten Objekt, das die [ITableData](itabledataiunknown.md) -Schnittstelle für die im _lppTable_ -Parameter zurückgegebene Tabelle verfügbar macht. Wenn kein Tabellendaten Objekt gewünscht wird, sollte _lppTblData_ auf NULL statt auf einen Zeigerwert festgelegt werden. 
    
## <a name="return-value"></a>Rückgabewert

Keine
  
## <a name="remarks"></a>Bemerkungen

MAPI verwendet die Funktionen, auf die durch _lpAllocateBuffer_, _lpAllocateMore_und _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und-Aufhebungen, insbesondere für die Zuweisung von Speicher für die Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::](imapiprop-getprops.md) GetProps und [IMAPITable:: QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Alles mögliche wird aus der Dialog-Ressource gelesen, einschließlich:
  
- Der Seitentitel, der das _ulbLpszLabel_ -Element der [DTBLPAGE](dtblpage.md) -Struktur aus dem Dialogfeldtitel in der Ressource liest. 
    
- Alle Steuerelement Titel das heißt, die _ulbLpszLabel_ -Elemente anderer Steuerelementstrukturen Lesen aus dem Steuerelementtext in der Ressource. 
    
 **BuildDisplayTable** überschreibt alles, was in den Eingabe Steuerstrukturen mit Informationen aus der Dialog-Ressource übergeben wurde, was besagt, dass der Aufrufer von **BuildDisplayTable** die Seiten-oder Steuerelement Titel nicht dynamisch angeben kann. Aufrufer, die dies tun müssen, können **BuildDisplayTable** das Tabellendaten Objekt in _lppTableData_ zurückgeben und Zeilen darin ändern; Sie können stattdessen die Anzeigetabelle manuell in einem Tabellendaten Objekt erstellen. 
  
Wenn _lppTableData_ nicht auf NULL festgelegt ist, ist der Anbieter für das Freigeben des Table-Datenobjekts verantwortlich, wenn es mit der Anzeigetabelle abgeschlossen ist. 
  

