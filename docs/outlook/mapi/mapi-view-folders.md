---
title: MAPI-Anzeigen von Ordnern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 194d62a645a5c641abc931db695b0d6acf0ac53a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579495"
---
# <a name="mapi-view-folders"></a>MAPI-Anzeigen von Ordnern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Anzeigen von Ordnern sind Stammordner, die zugeh�rigen Informationen zum Definieren der alternative Anzeigelayouts f�r den Inhalt von Nachrichtenordnern zwischen Personen (IPM) enthalten. Anzeigen von Ordnern befinden sich unter dem Stammverzeichnis f�r den Nachrichtenspeicher und werden daher nicht in der Clientanwendung typische angezeigt. Nicht bei jedem Nachrichtenspeicher umfasst Ordner anzeigen. nur Nachrichtenspeicher, die f�r die Verwendung als Standard-Informationsspeicher f�r die Sitzung konfiguriert sind, m�ssen diese enthalten.  
  
MAPI unterst�tzt zwei Anzeigen von Ordnern:
  
- Allgemeine � Der allgemeine Ansichtordner enth�lt Ansichten, die f�r den Nachrichtenspeicher standard und k�nnen von jedem Benutzer einen Client, der den Nachrichtenspeicher greift auf verwendet werden. Der Eintragsbezeichner für den allgemeinen Ansichtsordner wird in der **eigenschaft PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) des Speichers gespeichert.
    
- Privat � Der pers�nlichen Ansichtordner enth�lt Ansichten, die von einem bestimmten Benutzer definiert sind. MAPI definiert die **eigenschaft PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) zum Speichern des Eintragsbezeichners des persönlichen Ansichtsordners. Verwendung von pers�nlichen Ansichten, k�nnte ein Benutzer beispielsweise an eine Gruppe von Nachrichten sortiert nach Absender, nur Datum der Nachricht Betreff und des Empfangs auflisten aussehen; ein anderer Benutzer kann die gleiche Gruppe sortiert nach Datum, Betreff, Absender und Nachrichtengr��e auflisten betrachten.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Ordner](mapi-folders.md)

