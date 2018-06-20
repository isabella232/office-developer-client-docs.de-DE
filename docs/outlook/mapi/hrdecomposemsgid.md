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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3095907498b1ce7ae6b3666e0678dd0c5f76c23e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791903"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**Betrifft**: Outlook 
  
Trennt die ASCII-Darstellung des Bezeichners zusammengesetzter Eintrag eines Objekts in der Regel eine Meldung in einem Nachrichtenspeicher in die Eintrags-ID dieses Objekts im Speicher und den Store-Eintrags-ID an. 
  
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
  
> [in] Zeiger auf die Sitzung von der Clientanwendung verwendet. 
    
 _szMsgID_
  
> [in] Die Zeichenfolge, die Eintrags-ID des Objekts darstellt. 
    
 _pcbStoreEID_
  
> [out] Zeiger auf die zurückgegebene Größe in Bytes für die Eintrags-ID des Nachrichtenspeichers, die das Objekt enthält. Wenn der Parameter _SzMsgID_ auf eine noncompound Eintrags-ID zeigt eine Zeichenfolge, klicken Sie dann _PcbStoreEID_ -Parameter verweist auf 0 (null). 
    
 _ppStoreEID_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene Eintrags-ID des Nachrichtenspeichers, die das Objekt enthält. Wenn der Parameter _SzMsgID_ zu einer noncompound Eintrags-ID verweist, wird im Parameter _PpStoreEID_ NULL zurückgegeben. 
    
 _pcbMsgEID_
  
> [out] Zeiger auf die zurückgegebene Größe in Bytes für die Eintrags-ID des Objekts in seiner Store. Wenn der Parameter _SzMsgID_ auf eine Zeichenfolge noncompound Eintrag zeigt, ist der Parameter _PcbMsgEID_ gleich dem Wert des Parameters _CbEID_ . 
    
 _ppMsgEID_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene Eintrag Bezeichnerzeichenfolge des Objekts in seiner Store. Wenn der Parameter _SzMsgID_ auf einen Bezeichner noncompound Eintrag zeigt, verweist _PpMsgEID_ auf einen Zeiger auf eine konvertierte Kopie des Bezeichners noncompound Eintrag. 
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>Hinweise

Wenn vom _SzMsgID_ -Parameter angegebene Bezeichner zusammengesetzter ist, wird es von ASCII konvertiert und Teilen in die Eintrags-ID des Objekts in seiner Nachrichtenspeicher und den Store-Eintrags-ID. Noncompound Eintrags-ID-Zeichenfolgen werden einfach konvertiert und kopiert. Die zusammengesetzter Bezeichnerzeichenfolge getrennt werden ist normalerweise mit der Funktion [HrComposeMsgID](hrcomposemsgid.md) erstellt. 
  
Aufrufen der Funktion **HrDecomposeMsgID** entspricht dem Aufrufen der [HrEntryIDFromSz](hrentryidfromsz.md) und klicken Sie dann die Funktion [HrDecomposeEID](hrdecomposeeid.md) . 
  

