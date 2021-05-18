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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411246"
---
# <a name="imapisupportexpandrecips"></a>IMAPISupport::ExpandRecips

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Schließt die Empfängerliste einer Nachricht ab und erweitert bestimmte Verteilerlisten.
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> [in] Ein Zeiger auf die Nachricht, deren Empfängerliste verarbeitet werden soll.
    
 _lpulFlags_
  
> [out] Ein Zeiger auf eine Bitmaske von Flags, die den Typ der Verarbeitung steuert, die auftritt. Die folgenden Kennzeichen können festgelegt werden:
    
NEEDS_PREPROCESSING 
  
> Die Nachricht muss vor dem Senden vorverarbeitet werden.
    
NEEDS_SPOOLER 
  
> Der MAPI-Spooler (und nicht der Transportanbieter, an den der Anrufer eng gekoppelt ist) muss die Nachricht senden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Empfängerliste der Nachricht wurde erfolgreich verarbeitet.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::ExpandRecips-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter rufen **ExpandRecips auf,** um MAPI zum Ausführen der folgenden Aufgaben auffordern: 
  
- Erweitern Sie bestimmte persönliche Verteilerlisten auf ihre Komponentenempfänger.
    
- Ersetzen Sie alle Anzeigenamen, die geändert wurden, durch die ursprünglichen Namen.
    
- Markieren Sie alle doppelten Einträge.
    
- Lösen Sie alle einmal verwendeten Adressen auf. 
    
- Überprüfen Sie, ob die Nachricht vorverarbeitet werden muss, und legen Sie gegebenenfalls das Flag fest, auf das  _lpulFlags_ verweist, auf NEEDS_PREPROCESSING. 
    
 **ExpandRecips** erweitert alle Verteilerlisten mit dem Messagingadressentyp MAPIPDL. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **ExpandRecips immer** als Teil der Nachrichtenverarbeitung auf. Rufen Sie **ExpandRecips** einen der ersten Aufrufe in Ihrer [IMessage::SubmitMessage-Methodenimplementierung](imessage-submitmessage.md) auf. 
  
## <a name="see-also"></a>Siehe auch



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

