---
title: Datenträgerinstanzen und Cache Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d556ff4d-e2f3-4c83-a93f-b1bfda5abc8c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4f0b66476b1ab3d149b6f7e7b8171de7a509b597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338850"
---
# <a name="disk-instances-and-cache-tables"></a>Datenträgerinstanzen und Cache Tabellen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um ein Formular zu aktivieren, müssen die ausführbaren Dateien auf dem Computer des Benutzers verfügbar sein. Wenn Sie nicht verfügbar sind, müssen Sie aus der Formularbibliothek auf den lokalen Datenträger kopiert werden. Zu diesem Zweck erstellt der standardmäßige Formular-Manager ein Unterverzeichnis im Windows-Verzeichnis des Benutzers, das die ausführbaren Dateien des Formulars enthält (. Exe,. HLPs). Dieses Verzeichnis wird als Datenträger Instanz des Formulars bezeichnet.
  
Der standardmäßige Formular-Manager verwaltet eine Tabelle aller Datenträgerinstanzen, sodass eine Datenträger Instanz, die bereits vorhanden ist, verwendet werden kann, ohne dass Dateien aus der Formularbibliothek auf den Datenträger des Benutzers kopiert werden müssen. Die Tabelle der Datenträgerinstanzen wird als der am wenigsten verwendete Cache verwaltet. Wenn eine neue Datenträger Instanz benötigt wird, wird Sie auf den Computer des Benutzers kopiert, wobei die am wenigsten verwendete Datenträger Instanz ersetzt wird. Die Cache-Tabelle der Datenträger Instanz wird dann entsprechend der neuesten Konfiguration aktualisiert. Die Größe des Datenträgercaches ist eine vom benutzerkonfigurierbare Option, die es Benutzern ermöglicht, die Geschwindigkeit mit der verfügbaren Datenträgerkapazität auszugleichen.
  
Zusätzlich zum Cache der Datenträger Instanz verwaltet der standardmäßige Formular-Manager eine laufende Instanz-Tabelle, in der alle laufenden Instanzen von Formular Servern auf dem Computer des Benutzers aufgelistet sind. Dies verwendet die MAPI-Fähigkeit, Leerlauf Formular Instanzen in einem unsichtbaren Zustand zu halten, bis ein Formular der Nachrichtenklasse dieses Formular Servers aktiviert ist. Mit anderen Worten können Formularserver im RAM zwischengespeichert werden, um zu minimieren, wie oft die ausführbare Datei eines Formulars in einer Formularbibliothek gespeichert und vom Datenträger oder über das Netzwerk in den Arbeitsspeicher geladen werden muss. Wie der Datenträger Instanz-Cache verhält sich der Cache der laufenden Instanz in einer am wenigsten verwendeten Art und Weise so, dass eine laufende Formularinstanz aus dem Cache gelöscht werden kann, um Platz für eine andere Formularinstanz zu bilden. Dieser Cache wird nach einer aktiven Instanz eines Formular Servers durchsucht, bevor die Formularbibliotheken nach dem Formularserver durchsucht werden.
  
> [!NOTE]
> Der Standardformular-Manager zeigt beim Installieren eines Formulars auf der Arbeitsstation eines Benutzers eine Statusanzeige an, sodass der Benutzer den Vorgang abbrechen kann. Dies ist besonders nützlich, wenn sich die Verbindung des Benutzers mit der ausführbaren Datei des Formular Servers über einem Netzwerk mit niedriger Bandbreite befindet. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)

