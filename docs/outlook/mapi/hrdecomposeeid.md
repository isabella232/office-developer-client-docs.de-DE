---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b8b1f2d590616a30464181bde9bb0d0ad989bb5a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610818"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Trennt den zusammengesetzten Eintragsbezeichner eines Objekts, in der Regel eine Nachricht in einem Nachrichtenspeicher, in den Eintragsbezeichner dieses Objekts im Speicher und den Eintragsbezeichner des Informationsspeichers.
  
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
  
> [in] Zeiger auf die von der Clientanwendung verwendete Sitzung. 
    
 _cbEID_
  
> [in] Größe des zu trennenden zusammengesetzten Eintragsbezeichners in Bytes. 
    
 _pEID_
  
> [in] Zeiger auf den zu trennenden zusammengesetzten Eintragsbezeichner. 
    
 _"cursorStoreEID"_
  
> [out] Zeiger auf die zurückgegebene Größe des Eintragsbezeichners des Nachrichtenspeichers, der das Objekt enthält, in Bytes. Wenn der  _pEID-Parameter_ auf einen nicht kompatiblen Eintragsbezeichner zeigt, zeigt der  _parameter "storeEID"_ auf den Wert Null. 
    
 _ppStoreEID_
  
> [out] Zeiger auf einen Zeiger auf den zurückgegebenen Eintragsbezeichner des Nachrichtenspeichers, der das Objekt enthält. Wenn der  _pEID-Parameter_ auf einen nicht kompatiblen Eintragsbezeichner zeigt, wird NULL im  _PpStoreEID-Parameter_ zurückgegeben. 
    
 _msgEID_
  
> [out] Zeiger auf die zurückgegebene Größe des Eintragsbezeichners des Objekts in Bytes. Wenn der _pEID-Parameter_ auf einen Nichtcompound-Eintragsbezeichner zeigt, entspricht der _parameter "csvMsgEID"_ dem Wert des _cbEID-Parameters._ 
    
 _ppMsgEID_
  
> [out] Zeiger auf einen Zeiger auf den zurückgegebenen Eintragsbezeichner des Objekts. Wenn der  _pEID-Parameter_ auf einen Nichtcompound-Eintragsbezeichner zeigt, zeigt  _ppMsgEID_ auf einen Zeiger auf eine Kopie des Eintragsbezeichners, der nicht überkompound ist. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der durch den  _pEID-Parameter_ angegebene Bezeichner zusammengesetzt ist, wird er in den Eintragsbezeichner des Objekts innerhalb des Nachrichtenspeichers und den Eintragsbezeichner des Speichers aufgeteilt. Nicht kompatible Eintragsbezeichnerzeichenfolgen werden einfach kopiert. Der zusammengesetzte Bezeichner, der getrennt werden soll, ist in der Regel ein Bezeichner, der von der [HrComposeEID-Funktion](hrcomposeeid.md) erstellt wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Der Speicher, der den  _pEID-Parameter_ enthält, wird nach erfolgreichem Abschluss dieser Funktion freigegeben. Die aufrufende Implementierung ist für die Freigabe von Arbeitsspeicher für die Ausgabeparameter verantwortlich. 
  

