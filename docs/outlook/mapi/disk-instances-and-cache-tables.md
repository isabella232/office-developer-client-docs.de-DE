---
title: Datenträgerinstanzen und Cachetabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d556ff4d-e2f3-4c83-a93f-b1bfda5abc8c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 27b21162c53a64675abbf31a8ab512719b413d5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583162"
---
# <a name="disk-instances-and-cache-tables"></a>Datenträgerinstanzen und Cachetabellen

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Um ein Formular zu aktivieren, müssen die ausführbaren Dateien auf dem Computer des Benutzers verfügbar sein. Wenn sie nicht verfügbar sind, müssen sie aus der Bibliothek auf die lokale Festplatte kopiert werden. Zu diesem Zweck erstellt der Standard-Formular-Manager ein Unterverzeichnis im Windows-Verzeichnis des Benutzers enthält das Formular ausführbare Dateien (. EXE-Dateien. HLPs). Dieses Verzeichnis wird als Datenträger-Standardinstanz des Formulars bezeichnet.
  
Der Standard-Formular-Manager verwaltet eine Tabelle aller Instanzen der Datenträger, damit, wenn bereits eine Instanz Datenträger sie verwendet werden kann ohne Kopieren von Dateien aus der Bibliothek auf der Festplatte des Benutzers. Der Datenträger Instanzen die Tabelle wird als kleinsten häufig verwendete Cache verwaltet. Wenn eine neue Instanz des Datenträgers benötigt wird, wird es auf dem Computer des Benutzers, ersetzen die Instanz kleinsten häufig verwendete Datenträger kopiert. Die Datenträger Instanz Cachetabelle wird die aktuelle Konfiguration entsprechend aktualisiert. Die Größe der Datenträgercache ist eine vom Benutzer konfigurierbaren Option Benutzern ermöglichen, sich mit den verfügbaren Festplattenspeicherplatz Geschwindigkeit ausgeglichen.
  
Zusätzlich zu den Datenträgercache Instanz verwaltet der Standard-Formular-Manager eine ausgeführte Instanzentabelle, in der alle ausgeführte Instanzen des Formulars Server auf dem Computer des Benutzers aufgelistet. Dies verwendet MAPI Möglichkeit zum Formular im Leerlauf-Instanzen, die in einem unsichtbaren Zustand ausgeführt wird, bis ein Formular, das Formular des Servers Nachricht, dass die Klasse aktiviert ist. Anders ausgedrückt, können Formular Server zwischengespeichert werden sollen, im RAM, wie oft zu minimieren, ein Formular ausführbare Datei befindet sich innerhalb einer Formularbibliothek und in den Arbeitsspeicher vom Datenträger oder über das Netzwerk geladen werden muss. Der Datenträgercache Instanz Verhalten der ausgeführten Instanz Cache in einer Weise kleinsten häufig verwendet, damit eine ausgeführte Formularinstanz aus dem Zwischenspeicher um Platz für zu einer anderen Formularinstanz gelöscht werden kann. Dieser Cache wird für eine ausgeführte Instanz eines Formulars Servers durchsucht, bevor die Formularbibliotheken für den Server Formular durchsucht werden.
  
> [!NOTE]
> Der Standard-Formular-Manager zeigt eine Statusanzeige bei der Installation eines Formulars auf Arbeitsstation eines Benutzers, dem der Benutzer den Vorgang abzubrechen. Dies ist insbesondere dann hilfreich, wenn die Verbindung des Benutzers auf dem Formular Server ausführbare Datei über ein Netzwerk geringer Bandbreite ist. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)

