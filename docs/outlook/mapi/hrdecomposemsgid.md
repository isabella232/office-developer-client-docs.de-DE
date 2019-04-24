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
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348090"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Trennt die ASCII-Darstellung des verknüpften Eintrags Bezeichners eines Objekts, in der Regel eine Nachricht in einem Nachrichtenspeicher, in der Eintrags-ID des Objekts im Speicher und der Eintrags-ID des Speichers. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
   
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
  
> in Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird. 
    
 _szMsgID_
  
> in Die Zeichenfolge, die die Eintrags-ID des Objekts darstellt. 
    
 _pcbStoreEID_
  
> Out Zeiger auf die zurückgegebene Größe in Bytes des Eintrags Bezeichners des Nachrichtenspeichers, der das Objekt enthält. Wenn der _szMsgID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID-Zeichenfolge verweist, zeigt der Parameter _pcbStoreEID_ auf NULL. 
    
 _ppStoreEID_
  
> Out Zeiger auf einen Zeiger auf den zurückgegebenen Eintragsbezeichner des Nachrichtenspeichers, der das Objekt enthält. Wenn der _szMsgID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID verweist, wird NULL im _ppStoreEID_ -Parameter zurückgegeben. 
    
 _pcbMsgEID_
  
> Out Zeiger auf die zurückgegebene Größe in Bytes des Eintrags Bezeichners des Objekts innerhalb des Speichers. Wenn der _szMsgID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID-Zeichenfolge verweist, ist der _pcbMsgEID_ -Parameter gleich dem Wert des _cbEID_ -Parameters. 
    
 _ppMsgEID_
  
> Out Zeiger auf einen Zeiger auf die zurückgegebene Eintrags-ID-Zeichenfolge des Objekts innerhalb des Speichers. Wenn der _szMsgID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID zeigt, verweist _ppMsgEID_ auf einen Zeiger auf eine konvertierte Kopie des nicht verknüpften Eintrags Bezeichners. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Wenn der durch den _szMsgID_ -Parameter angegebene Bezeichner verknüpft ist, wird er aus ASCII konvertiert und in den Eintragsbezeichner des Objekts innerhalb des Nachrichtenspeichers und des Eintrags Bezeichners des Speichers aufgeteilt. Nicht zusammengesetzte Eintrags-ID-Zeichenfolgen werden einfach konvertiert und kopiert. Die zu Trenn Ende Verbund Bezeichner-Zeichenfolge wird in der Regel durch die [HrComposeMsgID](hrcomposemsgid.md) -Funktion erstellt. 
  
Das Aufrufen der **HrDecomposeMsgID** -Funktion entspricht dem Aufrufen der [HrEntryIDFromSz](hrentryidfromsz.md) -Funktion und dann der [HrDecomposeEID](hrdecomposeeid.md) -Funktion. 
  

