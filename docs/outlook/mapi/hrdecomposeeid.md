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
ms.openlocfilehash: d3ef8b61b6042d9c3e715168d9131a74facef000
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348069"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Trennt die verknüpfte Eintrags-ID eines Objekts, in der Regel eine Nachricht in einem Nachrichtenspeicher, in der Eintrags-ID des Objekts im Speicher und der Eintrags-ID des Speichers.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
   
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
  
> in Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird. 
    
 _cbEID_
  
> in Die Größe des verknüpften Eintrags Bezeichners in Byte, der getrennt werden soll. 
    
 _pEID_
  
> in Zeiger auf die verknüpfte Eintrags-ID, die getrennt werden soll. 
    
 _pcbStoreEID_
  
> Out Zeiger auf die zurückgegebene Größe in Bytes des Eintrags Bezeichners des Nachrichtenspeichers, der das Objekt enthält. Wenn der _pEID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID zeigt, zeigt der _pcbStoreEID_ -Parameter auf den Wert 0 (null). 
    
 _ppStoreEID_
  
> Out Zeiger auf einen Zeiger auf den zurückgegebenen Eintragsbezeichner des Nachrichtenspeichers, der das Objekt enthält. Wenn der _pEID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID verweist, wird NULL im _ppStoreEID_ -Parameter zurückgegeben. 
    
 _pcbMsgEID_
  
> Out Zeiger auf die zurückgegebene Größe in Bytes des Eintrags Bezeichners des Objekts. Wenn der _pEID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID zeigt, ist der _pcbMsgEID_ -Parameter gleich dem Wert des _cbEID_ -Parameters. 
    
 _ppMsgEID_
  
> Out Zeiger auf einen Zeiger auf den zurückgegebenen Eintragsbezeichner des Objekts. Wenn der _pEID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID zeigt, verweist _ppMsgEID_ auf einen Zeiger auf eine Kopie des nicht zusammengesetzten Eintrags Bezeichners. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Wenn der vom _pEID_ -Parameter angegebene Bezeichner Compound ist, wird er in den Eintragsbezeichner des Objekts innerhalb des Nachrichtenspeichers und die Eintrags-ID des Speichers aufgeteilt. Nicht zusammengesetzte Eintrags-ID-Zeichenfolgen werden einfach kopiert. Der zusammengesetzte Bezeichner, der getrennt werden soll, wird in der Regel durch die [HrComposeEID](hrcomposeeid.md) -Funktion erstellt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Der Speicher, der den _pEID_ -Parameter enthält, wird nach erfolgreichem Abschluss dieser Funktion freigegeben. Die aufrufende Implementierung ist für die Freigabe des Arbeitsspeichers für die Ausgabeparameter verantwortlich. 
  

