---
title: Verwalten einer Formularbibliothek
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9d249456ff95affc8af8ff720e3f8ee72e48d072
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567267"
---
# <a name="maintaining-a-form-library"></a>Verwalten einer Formularbibliothek

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Formularbibliothek enthält alle wichtigen Informationen zu einem Formular: seine Eigenschaften, verben und die ausführbaren Dateien des Servers. Einige Clients ermöglichen es ihren Benutzern, Formularserver zu verwalten, zu installieren oder zu entfernen. Wenn Sie dieses Feature Ihren Benutzern anbieten möchten, müssen Sie Zugriff auf Folgendes haben:
  
- Die Konfigurationsdatei des Formularservers, eine Datei mit der . CFG-Erweiterung.
    
- Das Containerobjekt der Formularbibliothek, ein Objekt, das die [IMAPIFormContainer : IUnknown-Schnittstelle](imapiformcontaineriunknown.md) implementiert. 
    
Um auf die Konfigurationsdatei oder einen Pfadnamen zu dieser zuzugreifen, verwenden Sie die praktischen Mittel. In der Regel stellen Clients dem Benutzer ein Dialogfeld zum Installieren und Entfernen von Formularservern vor, das auch verwendet werden kann, um den Benutzer zur Eingabe des Speicherorts der Konfigurationsdatei aufzufordern.
  
Um auf den Container der Formularbibliothek zuzugreifen, rufen Sie die [IMAPIFormMgr::OpenFormContainer-Methode](imapiformmgr-openformcontainer.md) des Formular-Managers auf. Übergeben Sie einen Enumerationswert, um anzugeben, welche Formularbibliothek geöffnet werden soll, und gegebenenfalls einen Zeiger auf das Objekt, das der Formular-Manager zum Öffnen der Formularbibliothek verwenden soll. Wenn Sie beispielsweise eine [Ordnerformularbibliothek](folder-form-libraries.md)öffnen, übergeben Sie einen [IMAPIFolder : IMAPIContainer-Zeiger.](imapifolderimapicontainer.md) 
  
Nachdem **OpenFormContainer** den **IMAPIFormContainer-Zeiger** zurückgegeben hat, rufen Sie entweder [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) oder [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md)auf, je nachdem, welche Wartung durchgeführt werden soll. **InstallForm** fügt der Bibliothek einen Formularserver hinzu. **RemoveForm** löscht einen Formularserver aus der Bibliothek. 
  

