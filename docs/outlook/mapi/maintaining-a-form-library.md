---
title: Verwalten einer Formularbibliothek
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 51c7c3f8ba70dcb3d35dc50806e984fd4b193818
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298460"
---
# <a name="maintaining-a-form-library"></a>Verwalten einer Formularbibliothek

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Formularbibliothek enthält alle wichtigen Informationen zu einem Formular: seine Eigenschaften, seine Verben und die ausführbaren Dateien des Servers. Einige Clients ermöglichen es Ihren Benutzern, Formularserver zu warten, zu installieren oder zu entfernen. Wenn Sie diese Funktion ihren Benutzern anbieten möchten, benötigen Sie Zugriff auf Folgendes:
  
- Die Konfigurationsdatei des Formular Servers, eine Datei mit der. CFG-Erweiterung.
    
- Das Container-Objekt der Formularbibliothek, ein Objekt, das die [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) -Schnittstelle implementiert. 
    
Um auf die Konfigurationsdatei oder einen Pfadnamen zu zugreifen, verwenden Sie alle Mittel, die bequem sind. In der Regel zeigen Clients dem Benutzer ein Dialogfeld zum Installieren und Entfernen von Formular Servern an, mit dem der Benutzer zur Bestätigung des Speicherorts der Konfigurationsdatei aufgefordert werden kann.
  
Um auf den Container der Formularbibliothek zuzugreifen, rufen Sie die [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) -Methode des Formular-Managers auf. Geben Sie einen Enumerationswert an, um anzugeben, welche Formularbibliothek geöffnet werden soll, und gegebenenfalls einen Zeiger auf das Objekt, das der Formular Manager zum Öffnen der Formularbibliothek verwenden soll. Wenn Sie beispielsweise eine [Ordner Formularbibliothek](folder-form-libraries.md)öffnen, führen Sie einen [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) -Zeiger aus. 
  
Nachdem **OpenFormContainer** den **IMAPIFormContainer** -Zeiger zurückgegeben hat, rufen Sie entweder [IMAPIFormContainer:: InstallForm](imapiformcontainer-installform.md) oder [IMAPIFormContainer:: RemoveForm](imapiformcontainer-removeform.md)auf, je nachdem, welche Wartung ausgeführt werden soll. **InstallForm** fügt der Bibliothek einen Formularserver hinzu; **RemoveForm** löscht einen Formularserver aus der Bibliothek. 
  

