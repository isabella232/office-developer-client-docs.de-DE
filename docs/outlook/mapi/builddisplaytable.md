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
  
Erstellt eine Anzeigetabelle aus den Eigenschaftenseitendaten, die in einer oder mehreren [DTPAGE-Strukturen enthalten](dtpage.md) sind. 
  
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
  
> [in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die zum Zuordnen von zusätzlichem Arbeitsspeicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freispeichern verwendet werden soll. 
    
 _lpMalloc_
  
> Nicht verwendet; sollte auf NULL festgelegt werden. 
    
 _hInstance_
  
> [in] Eine Instanz eines MAPI-Objekts, aus dem **BuildDisplayTable** Ressourcen abruft. 
    
 _cPages_
  
> [in] Anzahl der [DTPAGE-Strukturen](dtpage.md) im Array, auf die der  _lpPage-Parameter_ verweist. 
    
 _lpPage_
  
> [in] Zeiger auf ein Array von **DTPAGE-Strukturen,** die Informationen über die zu erstellende Anzeigetabelle enthalten. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format. 
    
 _lppTable_
  
> [out] Zeiger auf einen Zeiger auf die Anzeigetabelle, die die [IMAPITable-Schnittstelle verfügbar](imapitableiunknown.md) macht. 
    
 _lppTblData_
  
> [in, out] Zeiger auf einen Zeiger auf ein Tabellendatenobjekt, das die [ITableData-Schnittstelle](itabledataiunknown.md) in der im  _lppTable-Parameter_ zurückgegebenen Tabelle verfügbar machen soll. Wenn kein Tabellendatenobjekt gewünscht wird,  _sollte lppTblData_ auf NULL anstelle eines Zeigerwerts festgelegt werden. 
    
## <a name="return-value"></a>Rückgabewert

Keine
  
## <a name="remarks"></a>Hinweise

MAPI verwendet die Funktionen, auf die  _von lpAllocateBuffer_,  _lpAllocateMore_ und  _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und Deallocation, insbesondere zum Zuordnen von Arbeitsspeicher für Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Alles Mögliche wird aus der Dialogressource gelesen, einschließlich:
  
- Der Seitentitel, d. h. das  _ulbLpszLabel-Element_ der [DTBLPAGE-Struktur,](dtblpage.md) liest aus dem Dialogfeldtitel in der Ressource. 
    
- Alle Steuerelementtitel, d. h.  _die ulbLpszLabel-Elemente_ anderer Steuerelementstrukturen lesen aus dem Steuerelementtext in der Ressource. 
    
 **BuildDisplayTable** überschreibt alles, was in den Eingabesteuerelementstrukturen übergeben wird, mit Informationen aus der Dialogressource, was bedeutet, dass der Aufrufer von **BuildDisplayTable** Seiten- oder Steuerelementtitel nicht dynamisch angeben kann. Anrufer, die dies tun müssen, können **buildDisplayTable** das  _Tabellendatenobjekt in lppTableData_ zurückgeben und Zeilen ändern. oder sie können die Anzeigetabelle stattdessen in einem Tabellendatenobjekt von Hand erstellen. 
  
Wenn  _lppTableData_ nicht auf NULL festgelegt ist, ist der Anbieter dafür verantwortlich, das Tabellendatenobjekt frei zu machen, wenn es mit der Anzeigetabelle abgeschlossen ist. 
  

