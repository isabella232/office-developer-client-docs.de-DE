---
title: Struktur der Nachricht-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 58b6771c6bdae91ad0e496189258e4745de5bc84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584289"
---
# <a name="structure-of-message-store-providers"></a>Struktur der Nachricht-Anbieter
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Anbieter eine Nachricht bei der Ausführung im Arbeitsspeicher, ist eine [IMSProvider: IUnknown](imsprovideriunknown.md) Schnittstelle. Die **IMSProvider** -Schnittstelle ermöglicht Client-Anwendungen und die MAPI-Warteschlange an und von der Nachrichtenspeicher anmelden. Die, die Clientanwendungen und die MAPI-Warteschlange verwenden, Zugriff auf Ordner und Nachrichten im Nachrichtenspeicher sind [IMSLogon](imslogoniunknown.md) und [IMsgStore](imsgstoreimapiprop.md) Schnittstellen. Diese Schnittstellen werden normalerweise erstellt, wenn der Nachrichtenspeicher zuerst angemeldet ist, obwohl der Einstiegspunkt [MSProviderInit](msproviderinit.md) der Nachricht speichern DLL konnte auch erstellen sie. 
  
Da die **IMSLogon** und **IMsgStore** Schnittstellen einige Methoden gemeinsam nutzen, kann es einfacher sein ein Klassenobjekt erstellen, die beide Schnittstellen erbt. Sie können diese Schnittstellen in separaten Objekten implementieren, und Schreiben Hilfsfunktionen interne zur DLL, mit die die freigegebenen Methoden implementiert, die dann von den Methoden in den Schnittstellen **IMSLogon** und **IMsgStore** aufgerufen werden können. 
  
Die folgende Abbildung zeigt einen allgemeinen Überblick über die Objekthierarchie innerhalb eines Nachrichtenspeichers ausgeführt wird.
  
**Objekthierarchie des Nachrichtenspeichers**
  
![Objekthierarchie des Nachrichtenspeichers] (media/storeobj.gif "Objekthierarchie des Nachrichtenspeichers")
  
## <a name="see-also"></a>Siehe auch

- [Entwickeln eines Providers MAPI-Nachrichtenspeicher](developing-a-mapi-message-store-provider.md)

