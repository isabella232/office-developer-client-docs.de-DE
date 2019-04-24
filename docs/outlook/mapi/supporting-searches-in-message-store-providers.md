---
title: Unterstützen von Suchvorgängen in Nachrichtenspeicher Anbietern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 545047e90346b0f8e4a88eabcb20573f663f6d02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349588"
---
# <a name="supporting-searches-in-message-store-providers"></a>Unterstützen von Suchvorgängen in Nachrichtenspeicher Anbietern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Client Anwendungen verfügen häufig über einige Benutzeroberflächenkomponenten, die für die Suche nach Nachrichten in einem Nachrichtenspeicher vorgesehen sind. Suchkriterien werden in der [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) -Schnittstelle mithilfe der Methoden [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) und [IMAPIContainer:: GetSearchCriteria](imapicontainer-getsearchcriteria.md) angegeben. 
  
Clients verwenden die **PR_FINDER_ENTRYID** ([pidtagfinderentryid (](pidtagfinderentryid-canonical-property.md))-Eigenschaft des Nachrichtenspeicher Objekts, um den Stammordner im Nachrichtenspeicher zu identifizieren, der Ordner für Suchergebnisse enthält. Der Ordner Suchergebnisse ist häufig ein Ordner auf der obersten Ebene des Nachrichtenspeichers, der nicht Teil der IPM-Ordnerstruktur ist und daher ausgeblendet ist.
  
Ob der Nachrichtenspeicher Anbieter einen permanenten Suchergebnisordner verwendet oder einen erstellt, wenn ein Client die in der **PR_FINDER_ENTRYID** -Eigenschaft gespeicherte Eintrags-ID ist ein Implementierungsdetail. Es ist für den Nachrichtenspeicher Anbieter etwas einfacher, einen permanenten Ordner zu verwenden, der beim Erstellen des Nachrichtenspeichers erstellt wird, da dadurch die Komplikation beim Überprüfen der Eintrags-ID vermieden wird, wenn ein Ordner geöffnet wird, um zu sehen, ob ein Ordner Suchergebnisse. Allerdings können nicht alle Nachrichtenspeicher Anbieter dies tun; insbesondere werden schreibgeschützte Nachrichtenspeicher oder-Speicher, die eine MAPI-Schnittstelle zu einer Legacydatenbank bereitstellen, häufig nicht zugelassen oder können keinen permanenten Suchergebnisordner im zugrunde liegenden Speichermechanismus erstellen. 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

