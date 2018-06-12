---
title: MAPI-Anzeigen von Ordnern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cb26771e9968175ab67366e35cf019ce23d51b8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793106"
---
# <a name="mapi-view-folders"></a>MAPI-Anzeigen von Ordnern

  
  
**Betrifft**: Outlook 
  
Anzeigen von Ordnern sind Stammordner, die zugeh�rigen Informationen zum Definieren der alternative Anzeigelayouts f�r den Inhalt von Nachrichtenordnern zwischen Personen (IPM) enthalten. Anzeigen von Ordnern befinden sich unter dem Stammverzeichnis f�r den Nachrichtenspeicher und werden daher nicht in der Clientanwendung typische angezeigt. Nicht bei jedem Nachrichtenspeicher umfasst Ordner anzeigen. nur Nachrichtenspeicher, die f�r die Verwendung als Standard-Informationsspeicher f�r die Sitzung konfiguriert sind, m�ssen diese enthalten.  
  
MAPI unterst�tzt zwei Anzeigen von Ordnern:
  
- Allgemeine � Der allgemeine Ansichtordner enth�lt Ansichten, die f�r den Nachrichtenspeicher standard und k�nnen von jedem Benutzer einen Client, der den Nachrichtenspeicher greift auf verwendet werden. Die Eintrags-ID für den gemeinsamen Ansichtordner wird in den Speicher **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))-Eigenschaft gespeichert.
    
- Privat � Der pers�nlichen Ansichtordner enth�lt Ansichten, die von einem bestimmten Benutzer definiert sind. MAPI definiert die **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))-Eigenschaft die Eintrags-ID des Ordners persönliche Ansicht aufgenommen werden. Verwendung von pers�nlichen Ansichten, k�nnte ein Benutzer beispielsweise an eine Gruppe von Nachrichten sortiert nach Absender, nur Datum der Nachricht Betreff und des Empfangs auflisten aussehen; ein anderer Benutzer kann die gleiche Gruppe sortiert nach Datum, Betreff, Absender und Nachrichtengr��e auflisten betrachten.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Ordner](mapi-folders.md)

