---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 105219fe430cd8746c3aa6cf5cd90629d5f72080
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316527"
---
# <a name="imapisupportexpandrecips"></a>IMAPISupport::ExpandRecips

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vervollständigt die Empfängerliste einer Nachricht und erweitert bestimmte Verteilerlisten.
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> in Ein Zeiger auf die Nachricht, die die Empfängerliste hat, die verarbeitet werden soll.
    
 _lpulFlags_
  
> Out Ein Zeiger auf eine Bitmaske von Flags, die die Art der Verarbeitung steuert. Die folgenden Flags können festgelegt werden:
    
NEEDS_PREPROCESSING 
  
> Die Nachricht muss vorverarbeitet werden, bevor Sie gesendet wird.
    
NEEDS_SPOOLER 
  
> Die MAPI-Warteschlange (anstelle des Transportanbieters, an den der Aufrufer eng gekoppelt ist) muss die Nachricht senden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Empfängerliste der Nachricht wurde erfolgreich verarbeitet.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: ExpandRecips** -Methode wird für Support Objekte des Nachrichtenspeicher Anbieters implementiert. Nachrichtenspeicher Anbieter rufen **ExpandRecips** auf, um MAPI aufzufordern, die folgenden Aufgaben auszuführen: 
  
- Erweitern Sie bestimmte persönliche Verteilerlisten zu ihren Komponenten Empfängern.
    
- Ersetzen Sie alle Anzeigenamen, die mit den ursprünglichen Namen geändert wurden.
    
- Markieren Sie alle doppelten Einträge.
    
- Lösen Sie alle einmaligen Adressen. 
    
- Überprüfen Sie, ob die Nachricht eine Vorverarbeitung erfordert, und legen Sie, falls dies der Fall ist, die Kennzeichnung fest, auf die durch _lpulFlags_ auf NEEDS_PREPROCESSING verwiesen wird. 
    
 **ExpandRecips** erweitert alle Verteilerlisten mit dem Nachrichten Adresstyp MAPIPDL. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **ExpandRecips** immer als Teil der Nachrichtenverarbeitung auf. Rufen Sie einen der ersten Aufrufe in der **ExpandRecips** -Implementierung der [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode auf. 
  
## <a name="see-also"></a>Siehe auch



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

