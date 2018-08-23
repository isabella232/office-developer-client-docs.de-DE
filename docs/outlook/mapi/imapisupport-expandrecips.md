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
ms.openlocfilehash: 379fdc47f35fb183dd0bf551e421422abb106c0e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591010"
---
# <a name="imapisupportexpandrecips"></a>IMAPISupport::ExpandRecips

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Schließt eine Nachricht Empfängerliste bestimmten Verteilerlisten erweitern.
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> [in] Ein Zeiger auf die Nachricht mit der Empfängerliste verarbeitet werden.
    
 _lpulFlags_
  
> [out] Ein Zeiger auf eine Bitmaske aus Flags, die den Typ der Verarbeitung steuert, das auftritt. Die folgenden Kennzeichen können festgelegt werden:
    
NEEDS_PREPROCESSING 
  
> Die Nachricht muss vorverarbeitet werden, bevor es gesendet wird.
    
NEEDS_SPOOLER 
  
> Die MAPI-Warteschlange (anstelle der Adressbuchhierarchie, dem der Aufrufer eng verknüpft ist) muss die Nachricht zu senden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Liste der Empfänger die Nachricht wurde erfolgreich verarbeitet.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::ExpandRecips** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert. Nachricht Anbieter Aufrufen **ExpandRecips** um auffordern, MAPI, um die folgenden Aufgaben ausführen: 
  
- Erweitern Sie bestimmte persönlichen Verteilerlisten, an die Empfänger der Komponente.
    
- Ersetzen Sie alle Anzeigenamen, die geändert wurden mit den ursprünglichen Namen.
    
- Doppelte Einträge zu kennzeichnen.
    
- Alle einmalige-Adressen aufgelöst werden. 
    
- Überprüfen Sie, ob die Nachricht vorverarbeitung benötigt, und wenn dies der Fall ist, legen Sie das Flag auf _LpulFlags_ auf NEEDS_PREPROCESSING zeigt. 
    
 **ExpandRecips** erweitert alle Verteilerlisten, die den messaging Adresstyp MAPIPDL aufweisen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie immer **ExpandRecips** als Teil der Verarbeitung von Nachrichten. Rufen Sie **ExpandRecips** eine der ersten Aufrufe in der Implementierung der [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode. 
  
## <a name="see-also"></a>Siehe auch



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

