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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408803"
---
# <a name="maintaining-a-form-library"></a>Verwalten einer Formularbibliothek

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Formularbibliothek enthält alle wichtigen Informationen zu einem Formular: seine Eigenschaften, Verben und ausführbaren Dateien des Servers. Einige Clients ermöglichen benutzern das Warten, Installieren oder Entfernen von Formularservern. Wenn Sie diese Funktion Ihren Benutzern anbieten möchten, müssen Sie Zugriff auf:
  
- Die Konfigurationsdatei des Formularservers, eine Datei mit dem . CFG-Erweiterung.
    
- Das Containerobjekt der Formularbibliothek, ein Objekt, das die [IMAPIFormContainer : IUnknown-Schnittstelle](imapiformcontaineriunknown.md) implementiert. 
    
Um auf die Konfigurationsdatei oder einen Pfadnamen zu dieser zu zugreifen, verwenden Sie die praktischen Mittel. In der Regel stellen Clients dem Benutzer ein Dialogfeld zum Installieren und Entfernen von Formularservern vor, das auch verwendet werden kann, um den Benutzer zum Speicherort der Konfigurationsdatei aufforderen.
  
Um auf den Container der Formularbibliothek zu zugreifen, rufen Sie die [IMAPIFormMgr::OpenFormContainer-Methode](imapiformmgr-openformcontainer.md) des Formular-Managers auf. Übergeben Sie einen Enumerationswert, um anzugeben, welche Formularbibliothek geöffnet werden soll, und gegebenenfalls einen Zeiger auf das Objekt, mit dem der Formular-Manager die Formularbibliothek öffnen soll. Wenn Sie beispielsweise eine Ordnerformularbibliothek [öffnen,](folder-form-libraries.md)übergeben Sie einen [IMAPIFolder : IMAPIContainer-Zeiger.](imapifolderimapicontainer.md) 
  
Nachdem **OpenFormContainer** den **IMAPIFormContainer-Zeiger** zurückgegeben hat, rufen Sie [entweder IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) oder [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md)auf, je nachdem, wie die Wartung ausgeführt werden soll. **InstallForm** fügt der Bibliothek einen Formularserver hinzu. **RemoveForm** löscht einen Formularserver aus der Bibliothek. 
  

