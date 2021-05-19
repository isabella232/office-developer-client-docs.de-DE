---
title: Unterstützen von Suchdiensten in Store Anbietern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 545047e90346b0f8e4a88eabcb20573f663f6d02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425386"
---
# <a name="supporting-searches-in-message-store-providers"></a>Unterstützen von Suchdiensten in Store Anbietern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen verfügen häufig über einige Benutzeroberflächenkomponenten, die für die Suche nach Nachrichten in einem Nachrichtenspeicher verwendet werden. Suchkriterien werden in der [IMAPIContainer : IMAPIProp-Schnittstelle](imapicontainerimapiprop.md) mit den [Methoden IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) und [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) angegeben. 
  
Clients verwenden die PR_FINDER_ENTRYID **(** [PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) -Eigenschaft des Nachrichtenspeicherobjekts, um den Stammordner im Nachrichtenspeicher zu identifizieren, der Ordner für Suchergebnisse enthält. Der Suchergebnisordner ist häufig ein Ordner auf oberster Ebene des Nachrichtenspeichers, der nicht Teil der IPM-Ordnerstruktur ist und daher ausgeblendet ist.
  
Ob Ihr Nachrichtenspeicheranbieter einen permanenten Suchergebnisordner verwendet oder einen erstellt, wenn ein Client die in der **PR_FINDER_ENTRYID-Eigenschaft** gespeicherte Eintrags-ID öffnet, ist ein Implementierungsdetail. Es ist für Ihren Nachrichtenspeicheranbieter etwas einfacher, einen permanenten Ordner zu verwenden, der beim Erstellen des Nachrichtenspeichers erstellt wird, da dadurch die Komplikation vermieden wird, die Eintrags-ID zu überprüfen, wenn ein Ordner geöffnet wird, um festzustellen, ob ein Suchergebnisordner erstellt werden soll. Dies können jedoch nicht alle Nachrichtenspeicheranbieter tun. Insbesondere schreibgeschützte Nachrichtenspeicher oder -speicher, die eine MAPI-Schnittstelle für eine Ältere Datenbank bereitstellen, sind häufig nicht zulässig oder können keinen permanenten Suchergebnisordner im zugrunde liegenden Speichermechanismus erstellen. 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

