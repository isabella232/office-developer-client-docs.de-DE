---
title: Read-Only Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 752ff2d6-ca64-4507-adf1-4c054c321203
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 957a7f92963b97e5421bc801a3b046f098d6a08e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405338"
---
# <a name="read-only-message-stores"></a>Read-Only Nachrichtenspeicher

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Nachrichtenspeicher schreibgesch�tzt ist eine in die weder der MAPI-Client noch die MAPI-Warteschlange kann erstellen, �ndern oder l�schen Sie die Objekte im Nachrichtenspeicher. Es gibt viele Gr�nde, warum Sie m�glicherweise einen schreibgesch�tzten Nachrichtenspeicher implementieren m�chten. Beispielsweise konnte Credit reporting Firma einen nur-Lese-Speicher verwenden, um die Kunden oder Mitarbeiter finden Sie unter aber nicht �ndern einzelne Credit Berichte zu erm�glichen. Stellen Sie einen schreibgesch�tzten Nachrichtenspeicher Auswahl hat Auswirkungen auf f�r die Struktur des Anbieters und der Store selbst abzurufen. Beispielsweise ein Nachrichtenspeicher schreibgesch�tzt sind keinen Ordner Postausgang, da dann MAPI-Clients w�rde anfordern, dass neue ausgehende Nachrichten in diesem Ordner erstellt werden. In �hnlicher Weise ist es vom Informationsdienst daf�r verantwortlich, die Integrit�t der zugrunde liegende Speichermechanismus sicherzustellen.
  
Es gibt drei Flags, die in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Nachrichtenspeichers festgelegt werden können, die unterschiedliche Lesezugriffs Ebenen unterstützen. The STORE_READONLY flag indicates that all [IMAPIProp: IUnknown](imapipropiunknown.md) interfaces on objects in the message store are read-only. The STORE_MODIFY_OK flag indicates that existing messages in the message store may be modified, but new folders and messages may not be created. The STORE_CREATE_OK flag indicates that new messages and folders may be created, but indicates nothing about whether existing objects may be modified. 
  
Die Tatsache, dass MAPI-Clients und die MAPI-Warteschlange nicht m�glich ist, erstellen, �ndern oder L�schen von Objekten im Nachrichtenspeicher bedeutet nicht, dass den Inhalt der zugrunde liegende Speichermechanismus niemals �ndern. Noch bedeutet dies, dass Ihre Speicheranbieter nie Berechtigung in der zugrunde liegende Speichermechanismus zu schreiben muss. In einigen F�llen k�nnen diese beiden Bedingungen anwenden, jedoch nicht im Allgemeinen einer nur-Lese-Nachricht speichern. Die Zugriffsebene, dass ein Speicheranbieter erfordert und ob ein Speicheranbieter jemals Daten in der zugrunde liegende Speichermechanismus �ndert h�ngt im Wesentlichen die Art der einen Speicheranbieter.
  
Beispielsweise wenn Sie einen Anbieter anmelden, um MAPI-Clients Zugriff auf eine Datenbank auf einem CD-ROM-Ger�t gew�hren schreiben, der zugrunde liegende Speichermechanismus kann nicht ge�ndert werden und ein Speicheranbieter Leseberechtigung daf�r haben kann. Wenn jedoch Sie einen Anbieter anmelden schreiben, um MAPI-Clients schreibgesch�tzten Zugriff auf �ffentliche Ordner-Datenbank zu erm�glichen, Speicheranbieter muss jedoch zum Nachverfolgen von Nachrichten f�r jeden Benutzer, den gelesen/ungelesen Status m�ssen vom Informationsdienst neue Daten in der zugrunde liegende Speichermechanismus zu schreiben. Jedoch ist weder Beispiel Speicheranbieter jemals erforderlich, erstellen, �ndern oder L�schen von Ordnern und Nachrichten an die Anforderung des MAPI-Clients oder die MAPI-Warteschlange.
  
Die kleine Gruppe von Gr�nde, die ein Anbieter anmelden muss Daten in eine zugrunde liegende Speichermechanismus zu schreiben, die andernfalls schreibgesch�tzt ist, lautet wie folgt:
  
- Gelesen/ungelesen Status von Nachrichten gespeichert.
    
- Lese-/Nonread Benachrichtigungen zu implementieren. 
    
- Zum Speichern von Ansichten.
    
- Best�ndige Indizes f�r benutzerdefinierte Ordner Sortierreihenfolgen zwischengespeichert.
    
- To store the sort order of a folder's contents (supporting [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)).
    
- To store search criteria, search state, and results, if the message store provider supports searches (supporting [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)).
    
Wenn Ihre Nachricht Speicheranbieter nie Daten in der zugrunde liegende Speichermechanismus schreiben kann, m�ssen sie diese Features mithilfe eines separaten Speichermechanismus au�erhalb der zugrunde liegende Speichermechanismus implementieren. Beispielsweise k�nnte ein Anbieter f�r schreibgesch�tzte Nachricht anmelden gelesen/ungelesen Status von Nachrichten in den Speicher in einer Datei auf dem Computer des Benutzers speichern. Diese Strategie stellt zus�tzliche Schwierigkeiten aber m�glicherweise nur anteilm��ige wie f�r schreibgesch�tzte Nachricht Anbieter einige Funktionen zu implementieren. Halten den Inhalt des separater Speichervolumes Mechanismus mit den Objekten im Nachrichtenspeicher synchronisiert ist beispielsweise schwieriger als das Speichern des gelesen/ungelesen Status direkt in der Nachricht-Store selbst abzurufen.
  
Suche bietet eine zus�tzliche Schwierigkeit f�r schreibgesch�tzte Nachricht-Anbieter. Clients verwenden den in der **PR_FINDER_ENTRYID** ([pidtagfinderentryid (](pidtagfinderentryid-canonical-property.md))-Eigenschaft des Nachrichtenspeicher Objekts angegebenen Ordner, um den für Suchergebnisse verwendeten Ordner zu suchen. Schreibgesch�tzte Nachricht Anbieter installieren nicht h�ufig einen Ordner permanent Suchergebnisse in die Nachrichtenspeicher. In diesem Fall sollte der Nachricht Informationsdienst einen Eintrag Bezeichner in der **PR_FINDER_ENTRYID** -Eigenschaft speichern, die es erkennen kann, wenn Clients Ordner �ffnen, sodass es einen Suchergebnisse Ordner anstelle von Lesen aus der zugrunde liegende Speichermechanismus dynamisch erstellen kann. Da viele schreibgesch�tzte Nachricht Anbieter dynamisch allen Ordnern zu erstellen, ist dies jedoch in der Regel nicht zu viel in der Regel. 
  
In das Store-Anbieter-Objekt **PR_STORE_SUPPORT_MASK** -Eigenschaft ist die Tatsache, dass Ihre Nachricht Speicheranbieter schreibgesch�tzt ist angek�ndigt. Z�hlen Sie jedoch nicht auf Clients ber�cksichtigen diese Eigenschaft; einen Speicheranbieter Code sollte den schreibgesch�tzten Status der zugrunde liegende Speichermechanismus erzwingen. 
  
## <a name="see-also"></a>Siehe auch



[Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

