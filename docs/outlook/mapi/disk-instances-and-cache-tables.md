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
ms.openlocfilehash: 4f0b66476b1ab3d149b6f7e7b8171de7a509b597
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436755"
---
# <a name="disk-instances-and-cache-tables"></a>Datenträgerinstanzen und Cachetabellen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zum Aktivieren eines Formulars müssen die ausführbaren Dateien auf dem Computer des Benutzers verfügbar sein. Wenn sie nicht verfügbar sind, müssen sie aus der Formularbibliothek auf den lokalen Datenträger kopiert werden. Dazu erstellt der Standardformular-Manager ein Unterverzeichnis im Windows des Benutzers, das die ausführbaren Dateien des Formulars enthält (. EXEs,. HLPs). Dieses Verzeichnis wird als Datenträgerinstanz des Formulars bezeichnet.
  
Der Standardmäßige Formular-Manager verwaltet eine Tabelle aller Datenträgerinstanzen, sodass sie verwendet werden kann, wenn bereits eine Datenträgerinstanz vorhanden ist, ohne Dateien aus der Formularbibliothek auf den Datenträger des Benutzers kopieren zu müssen. Die Tabelle der Datenträgerinstanzen wird als am wenigsten häufig verwendeter Cache verwaltet. Wenn eine neue Datenträgerinstanz erforderlich ist, wird sie auf den Computer des Benutzers kopiert und ersetzt die am wenigsten häufig verwendete Datenträgerinstanz. Die Cachetabelle der Datenträgerinstanz wird dann entsprechend der neuesten Konfiguration aktualisiert. Die Größe des Datenträgercaches ist eine vom Benutzer konfigurierbare Option, mit der Benutzer die Geschwindigkeit mit der verfügbaren Datenträgerkapazität ausgleichen können.
  
Zusätzlich zum Datenträgerinstanzcache verwaltet der Standardformular-Manager eine ausgeführte Instanztabelle, in der alle ausgeführten Instanzen von Formularservern auf dem Computer des Benutzers aufgeführt sind. Dies nutzt die MapI-Fähigkeit, leerlaufformularinstanzen in einem unsichtbaren Zustand zu halten, bis eine Form der Nachrichtenklasse dieses Formularservers aktiviert wird. Mit anderen Worten, Formularserver können im RAM zwischengespeichert werden, um die Anzahl der ausführbaren Dateien eines Formulars in einer Formularbibliothek zu minimieren und vom Datenträger oder über das Netzwerk in den Arbeitsspeicher zu laden. Wie der Cache der Datenträgerinstanz verhält sich der ausgeführte Instanzcache am wenigsten häufig verwendet, sodass eine ausgeführte Formularinstanz aus dem Cache gelöscht werden kann, um Platz für eine andere Formularinstanz zu machen. Dieser Cache wird nach einer ausgeführten Instanz eines Formularservers durchsucht, bevor die Formularbibliotheken nach dem Formularserver durchsucht werden.
  
> [!NOTE]
> Der Standardformular-Manager zeigt beim Installieren eines Formulars auf der Arbeitsstation eines Benutzers eine Statusanzeige an, sodass der Benutzer den Vorgang abbrechen kann. Dies ist besonders hilfreich, wenn die Verbindung des Benutzers mit der ausführbaren Datei des Formularservers über ein Netzwerk mit niedriger Bandbreite liegt. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)

