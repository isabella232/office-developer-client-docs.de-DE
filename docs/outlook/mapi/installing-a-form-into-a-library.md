---
title: Installieren eines Formulars in eine Bibliothek
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 54b2dece31937b1ff233d4d1e7d8bbc198bfe118
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792705"
---
# <a name="installing-a-form-into-a-library"></a>Installieren eines Formulars in eine Bibliothek

  
  
**Betrifft**: Outlook 
  
Der standardmäßigen MAPI Formular-Manager mit dem Windows SDK bereitgestellte bietet keine Benutzeroberfläche für die Installation von Formularen in die verschiedenen Formularbibliotheken. Aus diesem Grund müssen Sie eine kleine Anwendung erstellen – oder detaillierte Anweisungen –, dass Benutzer verwenden können, um das Formular zu installieren.
  
Wenn Sie eine Installation Anwendung implementieren, muss der Reihe von Aktionen es führen Sie zum Installieren eines Formulars in einem Ordner zugeordneten Inhalt Tabelle lauten wie folgt:
  
1. Rufen Sie die [MAPIOpenFormMgr](mapiopenformmgr.md) -Funktion zum Öffnen des Formulars Manager. 
    
2. Verwenden Sie [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) oder [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) -Methode, um auszuwählen, und öffnen Sie den Zielcontainer für das Formular. 
    
3. Verwenden Sie die [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) -Funktion, um das Formular zu installieren. 
    
    Die Schritte 4 bis 6 sind für die Installation in einer lokalen Formularbibliothek:
    
4. Kopieren Sie alle Dateien an der entsprechenden Stelle auf dem lokalen Datenträger, wenn die Installation in der lokalen Formularbibliothek auf dem Computer des Benutzers ist. Bei Bedarf ändern Sie die Konfigurationsdatei Formular entsprechend der aktuellen Pfade der Komponenten. Die Konfigurationsdatei Formular kann relative Pfade enthalten, die in diesem Fall kann dieser Schritt nicht erforderlich sein.
    
5. Führen Sie die entsprechenden OLE-Registrierung Schritte aus, um den Formular-Server installiert wird den Nachrichtentyp zugeordnet.
    
6. Wenn das Formular in der lokalen Formularbibliothek installiert wurde, kopieren Sie des Formulars Symboldatei (ICO) und Konfigurationsdateien (cfg) in das Verzeichnis %WINDOWS%\FORMS\CONFIGS damit das Formular automatisch wiederhergestellt werden kann, falls die Formularbibliothek beschädigt oder gelöscht wird. Dieser Schritt ist das empfohlene jedoch nicht zwingend erforderlich.
    
> [!NOTE]
> Ersetzen die Schritte 1 und 2 mit einem Aufruf der Funktion [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) können Sie die Installation in einer lokalen Formularbibliothek vereinfachen. 
  
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formular-Servern](developing-mapi-form-servers.md)

