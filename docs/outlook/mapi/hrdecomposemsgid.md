---
title: HrDecomposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrDecomposeMsgID
api_type:
- COM
ms.assetid: 5e6a9f3e-79be-4ffd-9d42-3a14cabb1435
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3f6fd40860e6b86f8c3a79b14ab228052a972a89
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564253"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Trennt die ASCII-Darstellung des zusammengesetzten Eintragsbezeichners eines Objekts, in der Regel eine Nachricht in einem Nachrichtenspeicher, in den Eintragsbezeichner dieses Objekts im Speicher und den Eintragsbezeichner des Speichers. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
HrDecomposeMsgID(
  LPMAPISESSION psession,
  LPSTR szMsgID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a>Parameter

 _psession_
  
> [in] Zeiger auf die von der Clientanwendung verwendete Sitzung. 
    
 _szMsgID_
  
> [in] Die Zeichenfolge, die den Eintragsbezeichner des Objekts darstellt. 
    
 _"cursorStoreEID"_
  
> [out] Zeiger auf die zurückgegebene Größe des Eintragsbezeichners des Nachrichtenspeichers, der das Objekt enthält, in Bytes. Wenn der  _szMsgID-Parameter_ auf eine Zeichenfolge des Eintragsbezeichners ohne Kompound zeigt, zeigt der  _parameter "gitStoreEID"_ auf Null. 
    
 _ppStoreEID_
  
> [out] Zeiger auf einen Zeiger auf den zurückgegebenen Eintragsbezeichner des Nachrichtenspeichers, der das Objekt enthält. Wenn der  _szMsgID-Parameter_ auf einen Eintragsbezeichner ohne Kompound zeigt, wird NULL im  _PpStoreEID-Parameter_ zurückgegeben. 
    
 _msgEID_
  
> [out] Zeiger auf die zurückgegebene Größe des Eintragsbezeichners des Objekts innerhalb des Speichers in Byte. Wenn der _szMsgID-Parameter_ auf eine Zeichenfolge des Eintragsbezeichners ohne Kompound zeigt, entspricht der _parameter "csvMsgEID"_ dem Wert des _cbEID-Parameters._ 
    
 _ppMsgEID_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene Eintragsbezeichnerzeichenfolge des Objekts innerhalb seines Speichers. Wenn der  _szMsgID-Parameter_ auf einen Eintragsbezeichner ohne Kompound zeigt, zeigt  _ppMsgEID_ auf einen Zeiger auf eine konvertierte Kopie des Eintragsbezeichners, der den Eintrag nicht kompiliert. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der vom  _szMsgID-Parameter_ angegebene Bezeichner zusammengesetzt ist, wird er aus ASCII konvertiert und in den Eintragsbezeichner des Objekts innerhalb des Nachrichtenspeichers und des Eintragsbezeichners des Speichers aufgeteilt. Nicht kompatible Eintragsbezeichnerzeichenfolgen werden einfach konvertiert und kopiert. Die zu trennende zusammengesetzte Bezeichnerzeichenfolge ist in der Regel eine, die von der [HrComposeMsgID-Funktion](hrcomposemsgid.md) erstellt wird. 
  
Das Aufrufen der **HrDecomposeMsgID-Funktion** entspricht dem Aufrufen der [HrEntryIDFromSz-Funktion](hrentryidfromsz.md) und dann der [HrDecomposeEID-Funktion.](hrdecomposeeid.md) 
  

