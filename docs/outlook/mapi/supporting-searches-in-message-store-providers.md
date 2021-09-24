---
title: Unterstützen von Suchvorgängen in Nachrichtenanbietern Store
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b80b8e7593345f2f5e933dcc9e6d2d9f0770b6e7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549882"
---
# <a name="supporting-searches-in-message-store-providers"></a>Unterstützen von Suchvorgängen in Nachrichtenanbietern Store

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen verfügen häufig über einige Benutzeroberflächenkomponenten für die Suche nach Nachrichten in einem Nachrichtenspeicher. Suchkriterien werden in der [IMAPIContainer : IMAPIProp-Schnittstelle](imapicontainerimapiprop.md) mithilfe der Methoden [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) und [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) angegeben. 
  
Clients verwenden die eigenschaft **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) des Nachrichtenspeicherobjekts, um den Stammordner im Nachrichtenspeicher zu identifizieren, der Ordner für Suchergebnisse enthält. Der Suchergebnisordner ist häufig ein Ordner auf der obersten Ebene des Nachrichtenspeichers, der nicht Teil der IPM-Ordnerstruktur ist und daher ausgeblendet ist.
  
Ob Ihr Nachrichtenspeicheranbieter einen permanenten Suchergebnisordner verwendet oder einen erstellt, wenn ein Client den eintragsbezeichner öffnet, der in der **PR_FINDER_ENTRYID-Eigenschaft** gespeichert ist, ist ein Implementierungsdetail. Es ist für Ihren Nachrichtenspeicheranbieter etwas einfacher, einen permanenten Ordner zu verwenden, der beim Erstellen des Nachrichtenspeichers erstellt wird, da dadurch die Überprüfung des Eintragsbezeichners vermieden wird, wenn ein Ordner geöffnet wird, um festzustellen, ob ein Suchergebnisordner erstellt werden soll. Dies ist jedoch nicht für alle Nachrichtenspeicheranbieter möglich. Insbesondere schreibgeschützte Nachrichtenspeicher oder -speicher, die eine MAPI-Schnittstelle zu einer älteren Datenbank bereitstellen, sind häufig nicht zulässig oder können keinen permanenten Suchergebnisordner im zugrunde liegenden Speichermechanismus erstellen. 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

