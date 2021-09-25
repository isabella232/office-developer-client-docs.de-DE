---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: de652bef3325ca926e7827c15705dc2411b92fc7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556525"
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
  
> [out] Ein Zeiger auf eine Bitmaske mit Flags, die den Typ der ausgeführten Verarbeitung steuert. Die folgenden Flags können festgelegt werden:
    
NEEDS_PREPROCESSING 
  
> Die Nachricht muss vorverarbeitet werden, bevor sie gesendet wird.
    
NEEDS_SPOOLER 
  
> Der MAPI-Spooler (anstelle des Transportanbieters, mit dem der Aufrufer eng verbunden ist) muss die Nachricht senden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Empfängerliste der Nachricht wurde erfolgreich verarbeitet.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::ExpandRecips-Methode** ist für Supportobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter rufen **ExpandRecips** auf, um die MAPI aufzufordern, die folgenden Aufgaben auszuführen: 
  
- Erweitern Sie bestimmte persönliche Verteilerlisten auf ihre Komponentenempfänger.
    
- Ersetzen Sie alle Anzeigenamen, die geändert wurden, durch die ursprünglichen Namen.
    
- Markieren Sie alle doppelten Einträge.
    
- Auflösen aller einmaligen Adressen. 
    
- Überprüfen Sie, ob die Nachricht vorverarbeitet werden muss, und legen Sie, falls ja, das Flag, auf das von  _lpulFlags_ verwiesen wird, auf NEEDS_PREPROCESSING fest. 
    
 **ExpandRecips** erweitert alle Verteilerlisten mit dem Messaging-Adresstyp MAPIPDL. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **expandRecips** immer als Teil der Nachrichtenverarbeitung auf. Rufen Sie **expandRecips** einen der ersten Aufrufe in Ihrer [IMessage::SubmitMessage-Methodenimplementierungen](imessage-submitmessage.md) auf. 
  
## <a name="see-also"></a>Siehe auch



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

