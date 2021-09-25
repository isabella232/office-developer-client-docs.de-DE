---
title: Datenträgerinstanzen und Cachetabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d556ff4d-e2f3-4c83-a93f-b1bfda5abc8c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 58285c4b9ca4752645e1aa378cd8e51d59095a88
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576387"
---
# <a name="disk-instances-and-cache-tables"></a>Datenträgerinstanzen und Cachetabellen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zum Aktivieren eines Formulars müssen die ausführbaren Dateien auf dem Computer des Benutzers verfügbar sein. Wenn sie nicht verfügbar sind, müssen sie aus der Formularbibliothek auf den lokalen Datenträger kopiert werden. Hierzu erstellt der Standardformular-Manager ein Unterverzeichnis im Windows Verzeichnis des Benutzers, das die ausführbaren Dateien () des Formulars enthält. Exes. HLPs). Dieses Verzeichnis wird als Datenträgerinstanz des Formulars bezeichnet.
  
Der Standardformular-Manager verwaltet eine Tabelle aller Datenträgerinstanzen, sodass eine bereits vorhandene Datenträgerinstanz verwendet werden kann, ohne Dass Dateien aus der Formularbibliothek auf den Datenträger des Benutzers kopiert werden müssen. Die Tabelle der Datenträgerinstanzen wird als Cache verwaltet, der am seltensten verwendet wird. Wenn eine neue Datenträgerinstanz erforderlich ist, wird sie auf den Computer des Benutzers kopiert und ersetzt die am seltensten verwendete Datenträgerinstanz. Die Cachetabelle der Datenträgerinstanz wird dann aktualisiert, um die neueste Konfiguration widerzuspiegeln. Die Größe des Datenträgercaches ist eine vom Benutzer konfigurierbare Option, mit der Benutzer die Geschwindigkeit mit der verfügbaren Datenträgerkapazität abgleichen können.
  
Zusätzlich zum Cache der Datenträgerinstanz verwaltet der Standardformular-Manager eine ausgeführte Instanztabelle, die alle ausgeführten Instanzen von Formularservern auf dem Computer des Benutzers auflistet. Dadurch wird die MAPI-Fähigkeit verwendet, leerlaufaktive Formularinstanzen in einem unsichtbaren Zustand zu halten, bis ein Formular der Nachrichtenklasse dieses Formularservers aktiviert wird. Mit anderen Worten, Formularserver können im RAM zwischengespeichert werden, um zu minimieren, wie oft sich die ausführbare Datei eines Formulars in einer Formularbibliothek befinden und vom Datenträger oder über das Netzwerk in den Arbeitsspeicher geladen werden muss. Wie der Cache der Datenträgerinstanz verhält sich der cache der ausgeführten Instanz auf die am wenigsten häufig verwendete Weise, sodass eine ausgeführte Formularinstanz aus dem Cache gelöscht werden kann, um Platz für eine andere Formularinstanz zu schaffen. Dieser Cache wird nach einer ausgeführten Instanz eines Formularservers durchsucht, bevor die Formularbibliotheken nach dem Formularserver durchsucht werden.
  
> [!NOTE]
> Der Standardformular-Manager zeigt beim Installieren eines Formulars auf der Arbeitsstation eines Benutzers eine Statusanzeige an, sodass der Benutzer den Vorgang abbrechen kann. Dies ist besonders nützlich, wenn sich die Verbindung des Benutzers mit der ausführbaren Datei des Formularservers über ein Netzwerk mit geringer Bandbreite befindet. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)

