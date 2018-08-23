---
title: Pflegen einer Formularbibliothek
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6713055837e3b9b664d5fa1465c9a889919ee5ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590092"
---
# <a name="maintaining-a-form-library"></a>Pflegen einer Formularbibliothek

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine Formularbibliothek enthält alle wichtigen Informationen zu einem Formular: seine Eigenschaften, seiner Verben und ausführbare Dateien des Servers. Einige Clients können ihre Benutzer verwalten, installieren oder Entfernen von Servern Formular. Wenn Sie dieses Feature Ihren Benutzern anbieten möchten, benötigen Sie Zugriff auf:
  
- Der Formular-Server-Konfigurationsdatei, eine Datei mit der. Erweiterung CFG.
    
- Der Formularbibliothek Container-Objekt, ein Objekt, das implementiert die [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) Schnittstelle. 
    
Zugriff auf die Konfigurationsdatei oder einen Pfadnamen zu verwenden sind beliebige Weise praktisch. Clients stehen in der Regel dem Benutzer ein Dialogfeld zum Installieren und Entfernen von Servern Formular, die auch verwendet werden können, um den Benutzer für den Speicherort der Konfigurationsdatei aufzufordern.
  
Rufen Sie den Formular-Manager [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) -Methode, um für den Zugriff auf die Formularbibliothek Container. Übergeben Sie eine Enumerationswert an, welche Formularbibliothek zu öffnen, und Sie bei Bedarf einen Zeiger auf das Objekt, das der Formular-Manager zum Öffnen der Formularbibliothek verwendet werden soll. Wenn Sie einen [Ordner von Formularbibliotheken](folder-form-libraries.md)öffnen, beispielsweise übergeben ein [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) Zeiger. 
  
Nach dem **OpenFormContainer** den **IMAPIFormContainer** Zeiger zurückgegeben wird, rufen Sie [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) oder [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), je nach der Wartung ausgeführt werden. **InstallForm** hinzugefügt der Bibliothek einen Formular Server; **RemoveForm** Löscht einen Formular Server aus der Bibliothek. 
  

