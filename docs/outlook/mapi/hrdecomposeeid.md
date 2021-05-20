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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d3ef8b61b6042d9c3e715168d9131a74facef000
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436111"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Trennt die zusammengesetzte Eintrags-ID eines Objekts, in der Regel eine Nachricht in einem Nachrichtenspeicher, in die Eintrags-ID dieses Objekts im Speicher und den Eintragsbezeichner des Speichers.
  
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
  
> [in] Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird. 
    
 _cbEID_
  
> [in] Die Größe des zusammengesetzten Eintragsbezeichners, der getrennt werden soll, in Bytes. 
    
 _pEID_
  
> [in] Zeiger auf den zusammengesetzten Eintragsbezeichner, der getrennt werden soll. 
    
 _pcbStoreEID_
  
> [out] Zeiger auf die zurückgegebene Größe des Eintragsbezeichners des Nachrichtenspeichers, der das Objekt enthält, in Bytes. Wenn der  _pEID-Parameter_ auf einen Nichtcompound-Eintragsbezeichner verweist, zeigt der  _parameter "pcbStoreEID"_ auf den Wert Null. 
    
 _ppStoreEID_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene Eintrags-ID des Nachrichtenspeichers, der das Objekt enthält. Wenn der  _pEID-Parameter_ auf einen Nichtcompound-Eintragsbezeichner verweist, wird NULL im  _ppStoreEID-Parameter_ zurückgegeben. 
    
 _pcbMsgEID_
  
> [out] Zeiger auf die zurückgegebene Größe des Eintragsbezeichners des Objekts in Bytes. Wenn der _pEID-Parameter_ auf einen Nichtcompound-Eintragsbezeichner verweist, entspricht der _parameter "pcbMsgEID"_ dem Wert des _cbEID-Parameters._ 
    
 _ppMsgEID_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene Eintrags-ID des Objekts. Wenn der  _pEID-Parameter_ auf einen Nichtcompound-Eintragsbezeichner verweist, zeigt  _ppMsgEID_ auf einen Zeiger auf eine Kopie der Nichtcompound-Eintrags-ID. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Hinweise

Wenn der durch den  _pEID-Parameter_ angegebene Bezeichner zusammengesetzt ist, wird er in den Eintragsbezeichner des Objekts innerhalb des Nachrichtenspeichers und den Eintragsbezeichner des Speichers aufgeteilt. Nichtkompounde Eingabebezeichnerzeichenfolgen werden einfach kopiert. Der zusammengesetzte Bezeichner, der getrennt werden soll, ist in der Regel eine, die von der [HrComposeEID-Funktion erstellt](hrcomposeeid.md) wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Der Speicher, der den  _pEID-Parameter_ enthält, wird nach erfolgreichem Abschluss dieser Funktion freigegeben. Die aufrufende Implementierung ist für das Freispeichern von Arbeitsspeicher für die Ausgabeparameter verantwortlich. 
  

