---
title: BuildDisplayTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- BuildDisplayTable
api_type:
- HeaderDef
ms.assetid: 0846415b-6fe1-4504-8620-108af6719015
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c49d7176b74d2d6fafd3da0a4d658dd72c7b54c8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621157"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine Anzeigetabelle aus den Eigenschaftenseitendaten, die in einer oder mehreren [DTPAGE-Strukturen](dtpage.md) enthalten sind. 
  
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
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die verwendet werden soll, um zusätzlichen Speicher zuzuweisen. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freigeben von Arbeitsspeicher verwendet werden soll. 
    
 _lpMalloc_
  
> Nicht verwendet; sollte auf NULL festgelegt werden. 
    
 _Hinstance_
  
> [in] Eine Instanz eines MAPI-Objekts, aus dem **BuildDisplayTable** Ressourcen abruft. 
    
 _cPages_
  
> [in] Anzahl der [DTPAGE-Strukturen](dtpage.md) im Array, auf das der  _lpPage-Parameter_ verweist. 
    
 _lpPage_
  
> [in] Zeiger auf ein Array von **DTPAGE-Strukturen,** die Informationen zu den zu erstellenden Anzeigetabellenseiten enthalten. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format. 
    
 _lppTable_
  
> [out] Zeiger auf einen Zeiger auf die Anzeigetabelle, die die [IMAPITable-Schnittstelle](imapitableiunknown.md) verfügbar macht. 
    
 _lppTblData_
  
> [in, out] Zeiger auf einen Zeiger auf ein Tabellendatenobjekt, das die [ITableData-Schnittstelle](itabledataiunknown.md) für die im  _lppTable-Parameter_ zurückgegebene Tabelle verfügbar machen kann. Wenn kein Tabellendatenobjekt gewünscht wird, sollte  _lppTblData_ anstelle eines Zeigerwerts auf NULL festgelegt werden. 
    
## <a name="return-value"></a>Rückgabewert

Keines
  
## <a name="remarks"></a>Bemerkungen

DIE MAPI verwendet die Funktionen, auf die von _lpAllocateBuffer_, _lpAllocateMore_ und _lpFreeBuffer_ für die meisten Speicherzuweisungen und -zuordnungen verwiesen wird, insbesondere zum Zuordnen von Arbeitsspeicher zur Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows.](imapitable-queryrows.md) 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Alles Mögliche wird aus der Dialogressource gelesen, einschließlich:
  
- Der Seitentitel, d. h. das  _UlbLpszLabel-Element_ der [DTBLPAGE-Struktur,](dtblpage.md) das aus dem Dialogtitel in der Ressource gelesen wird. 
    
- Alle Steuerelementtitel, d. h. die  _ulbLpszLabel-Elemente_ anderer Steuerelementstrukturen, lesen aus dem Steuerelementtext in der Ressource. 
    
 **BuildDisplayTable** überschreibt alle in den Eingabesteuerungsstrukturen übergebenen Elemente mit Informationen aus der Dialogressource, was bedeutet, dass der Aufrufer von **BuildDisplayTable** Seiten- oder Steuerelementtitel nicht dynamisch angeben kann. Aufrufer, die dies tun müssen, können **buildDisplayTable** das Tabellendatenobjekt in  _lppTableData_ zurückgeben und Zeilen darin ändern. oder sie können die Anzeigetabelle stattdessen von Hand in einem Tabellendatenobjekt erstellen. 
  
Wenn  _lppTableData_ nicht auf NULL festgelegt ist, ist der Anbieter für die Freigabe des Tabellendatenobjekts verantwortlich, wenn es mit der Anzeigetabelle fertig ist. 
  

