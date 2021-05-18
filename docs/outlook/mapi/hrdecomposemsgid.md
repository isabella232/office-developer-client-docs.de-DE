---
title: HrDecomposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeMsgID
api_type:
- COM
ms.assetid: 5e6a9f3e-79be-4ffd-9d42-3a14cabb1435
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404435"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Trennt die ASCII-Darstellung des zusammengesetzten Eintragsbezeichners eines Objekts , in der Regel eine Nachricht in einem Nachrichtenspeicher, in den Eintragsbezeichner dieses Objekts im Speicher und den Eintragsbezeichner des Speichers. 
  
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
  
> [in] Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird. 
    
 _szMsgID_
  
> [in] Die Zeichenfolge, die den Eintragsbezeichner des Objekts darstellt. 
    
 _pcbStoreEID_
  
> [out] Zeiger auf die zurückgegebene Größe des Eintragsbezeichners des Nachrichtenspeichers, der das Objekt enthält, in Bytes. Wenn der  _szMsgID-Parameter_ auf eine Nichtkompound-Eintrags-ID-Zeichenfolge zeigt, zeigt der  _Parameter "pcbStoreEID"_ auf Null. 
    
 _ppStoreEID_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene Eintrags-ID des Nachrichtenspeichers, der das Objekt enthält. Wenn der  _parameter szMsgID_ auf einen Nichtcompound-Eintragsbezeichner verweist, wird NULL im  _ppStoreEID-Parameter_ zurückgegeben. 
    
 _pcbMsgEID_
  
> [out] Zeiger auf die zurückgegebene Größe des Eintragsbezeichners des Objekts im Speicher in Bytes. Wenn der _parameter szMsgID_ auf eine Nichtkompound-Eintrags-ID-Zeichenfolge verweist, entspricht der _parameter "pcbMsgEID"_ dem Wert des _cbEID-Parameters._ 
    
 _ppMsgEID_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene Eintragsbezeichnerzeichenfolge des Objekts in seinem Speicher. Wenn der  _szMsgID-Parameter_ auf einen Nichtcompound-Eintragsbezeichner verweist, zeigt  _ppMsgEID_ auf einen Zeiger auf eine konvertierte Kopie der Nichtcompound-Eintrags-ID. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Hinweise

Wenn der durch den  _szMsgID-Parameter_ angegebene Bezeichner zusammengesetzt ist, wird er aus ASCII konvertiert und in den Eintragsbezeichner des Objekts innerhalb des Nachrichtenspeichers und den Eintragsbezeichner des Speichers aufgeteilt. Nichtkompounde Eingabebezeichnerzeichenfolgen werden einfach konvertiert und kopiert. Die zu trennende Zeichenfolge für zusammengesetzte Bezeichner ist in der Regel eine, die von der [HrComposeMsgID-Funktion erstellt](hrcomposemsgid.md) wird. 
  
Das Aufrufen **der HrDecomposeMsgID-Funktion** entspricht dem Aufrufen der [HrEntryIDFromSz-Funktion](hrentryidfromsz.md) und dann der [HrDecomposeEID-Funktion.](hrdecomposeeid.md) 
  

