---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e66d48b6caefe0fee67f41ea829db3201751cf27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791914"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

  
  
**Betrifft**: Outlook 
  
Trennt die zusammengesetzter Eintrags-ID eines Objekts in der Regel eine Meldung in einem Nachrichtenspeicher in die Eintrags-ID dieses Objekts im Speicher und den Store-Eintrags-ID an.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
HrDecomposeEID(
  LPMAPISESSION psession,
  ULONG cbEID,
  LPENTRYID pEID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a>Parameter

 _psession_
  
> [in] Zeiger auf die Sitzung von der Clientanwendung verwendet. 
    
 _cbEID_
  
> [in] Größe in Bytes des Bezeichners zusammengesetzter Eintrag getrennt werden. 
    
 _pEID_
  
> [in] Zeiger auf den Eintrag zusammengesetzter Bezeichner getrennt werden. 
    
 _pcbStoreEID_
  
> [out] Zeiger auf die zurückgegebene Größe in Bytes für die Eintrags-ID des Nachrichtenspeichers, die das Objekt enthält. Wenn der Parameter _pEID_ auf eine noncompound Eintrags-ID verweist, verweist der Parameter _PcbStoreEID_ auf den Wert 0 (null). 
    
 _ppStoreEID_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene Eintrags-ID des Nachrichtenspeichers, die das Objekt enthält. Wenn der Parameter _pEID_ auf eine noncompound Eintrags-ID verweist, wird im Parameter _PpStoreEID_ NULL zurückgegeben. 
    
 _pcbMsgEID_
  
> [out] Zeiger auf die zurückgegebene Größe, der die Eintrags-ID des Objekts in Bytes. Wenn der Parameter _pEID_ auf einen Bezeichner noncompound Eintrag zeigt, ist der Parameter _PcbMsgEID_ gleich dem Wert des Parameters _CbEID_ . 
    
 _ppMsgEID_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene Eintrags-ID des Objekts. Wenn der Parameter _pEID_ auf eine noncompound Eintrags-ID verweist, verweist _PpMsgEID_ auf einen Zeiger auf eine Kopie des Bezeichners noncompound Eintrag. 
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>Hinweise

Wenn vom _pEID_ -Parameter angegebene Bezeichner zusammengesetzter ist, wird es in die Eintrags-ID des Objekts in seiner Nachrichtenspeicher und den Store-Eintrags-ID unterteilt. Noncompound Eintrags-ID-Zeichenfolgen werden einfach kopiert. Der zusammengesetzte Bezeichner, der getrennt werden ist in der Regel durch die Funktion [HrComposeEID](hrcomposeeid.md) erstellt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nach dem erfolgreichen Abschluss dieser Funktion wird der Speicher, der den Parameter _pEID enthält,_ freigegeben. Die aufrufende Implementierung ist verantwortlich für die Freigabe von Speicher für die Ausgabeparameter. 
  

