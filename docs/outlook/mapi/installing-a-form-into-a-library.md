---
title: Installieren eines Formulars in einer Bibliothek
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 808bf3b934e05d4f7d856986fa5ead299a247d05
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630523"
---
# <a name="installing-a-form-into-a-library"></a>Installieren eines Formulars in einer Bibliothek

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der mit dem Windows SDK bereitgestellte MAPI-Formular-Manager bietet keine Benutzeroberfläche zum Installieren von Formularen in den verschiedenen Formularbibliotheken. Aus diesem Grund müssen Sie eine kleine Anwendung oder detaillierte Anweisungen erstellen, die Benutzer zum Installieren des Formulars verwenden können.
  
Wenn Sie eine Installationsanwendung implementieren, müssen Sie eine Reihe von Aktionen ausführen, um ein Formular im zugeordneten Inhaltsverzeichnis eines Ordners zu installieren:
  
1. Rufen Sie die [MAPIOpenFormMgr-Funktion](mapiopenformmgr.md) auf, um den Formular-Manager zu öffnen. 
    
2. Verwenden Sie [DIE IMAPIFormMgr::OpenFormContainer-](imapiformmgr-openformcontainer.md) oder [IMAPIFormMgr::SelectFormContainer-Methode,](imapiformmgr-selectformcontainer.md) um den Zielcontainer für das Formular auszuwählen und zu öffnen. 
    
3. Verwenden Sie die [IMAPIFormContainer::InstallForm-Funktion,](imapiformcontainer-installform.md) um das Formular zu installieren. 
    
    Die Schritte 4 bis 6 dienen zur Installation in einer lokalen Formularbibliothek:
    
4. Kopieren Sie alle Dateien an die entsprechende Stelle auf dem lokalen Datenträger, wenn die Installation in der lokalen Formularbibliothek auf der Arbeitsstation des Benutzers erfolgt. Ändern Sie bei Bedarf die Formularkonfigurationsdatei, um die aktuellen Pfade von Komponenten widerzuspiegeln. Die Formularkonfigurationsdatei kann relative Pfade enthalten, in diesem Fall ist dieser Schritt möglicherweise nicht erforderlich.
    
5. Führen Sie die entsprechenden OLE-Registrierungsschritte aus, um den Nachrichtentyp dem installierten Formularserver zuzuordnen.
    
6. Wenn das Formular in der lokalen Formularbibliothek installiert wurde, kopieren Sie die Symbol- und Konfigurationsdateien (CFG) des Formulars in das Verzeichnis %WINDOWS%\FORMS\CONFIGS, damit das Formular automatisch wiederhergestellt werden kann, falls die Formularbibliothek beschädigt oder gelöscht ist. Dieser Schritt wird empfohlen, ist jedoch nicht obligatorisch.
    
> [!NOTE]
> Sie können die Installation in einer lokalen Formularbibliothek vereinfachen, indem Sie die Schritte 1 und 2 durch einen Aufruf der [MAPIOpenLocalFormContainer-Funktion](mapiopenlocalformcontainer.md) ersetzen. 
  
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

