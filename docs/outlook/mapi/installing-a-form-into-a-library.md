---
title: Installieren eines Formulars in einer Bibliothek
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 08470a80153e42136922ae502252d83de0125512
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433143"
---
# <a name="installing-a-form-into-a-library"></a>Installieren eines Formulars in einer Bibliothek

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der standardmäßige MAPI-Formular-Manager, der mit dem Windows SDK bereitgestellt wird, stellt keine Benutzeroberfläche zum Installieren von Formularen in den verschiedenen Formularbibliotheken bereit. Aus diesem Grund müssen Sie eine kleine Anwendung oder detaillierte Anweisungen erstellen, die Benutzer zum Installieren des Formulars verwenden können.
  
Wenn Sie eine Installationsanwendung implementieren, sind die folgenden Aktionen erforderlich, um ein Formular in der zugehörigen Inhaltstabelle eines Ordners zu installieren:
  
1. Rufen Sie die [MAPIOpenFormMgr-Funktion](mapiopenformmgr.md) auf, um den Formular-Manager zu öffnen. 
    
2. Verwenden [Sie die IMAPIFormMgr::OpenFormContainer-](imapiformmgr-openformcontainer.md) oder [IMAPIFormMgr::SelectFormContainer-Methode,](imapiformmgr-selectformcontainer.md) um den Zielcontainer für das Formular auszuwählen und zu öffnen. 
    
3. Verwenden Sie die [IMAPIFormContainer::InstallForm-Funktion,](imapiformcontainer-installform.md) um das Formular zu installieren. 
    
    Die Schritte 4 bis 6 sind für die Installation in einer lokalen Formularbibliothek:
    
4. Kopieren Sie alle Dateien an den entsprechenden Ort auf dem lokalen Datenträger, wenn die Installation in der lokalen Formularbibliothek auf der Arbeitsstation des Benutzers erfolgt. Ändern Sie bei Bedarf die Formularkonfigurationsdatei, um die aktuellen Pfade von Komponenten widerspiegeln zu können. Die Formularkonfigurationsdatei kann relative Pfade enthalten, in diesem Fall ist dieser Schritt möglicherweise nicht erforderlich.
    
5. Führen Sie die entsprechenden OLE-Registrierungsschritte aus, um den Nachrichtentyp dem zu installierende Formularserver zuzuordnen.
    
6. Wenn das Formular in der lokalen Formularbibliothek installiert wurde, kopieren Sie das Symbol (.ico) und die Konfigurationsdateien (CFG) des Formulars in das Verzeichnis %WINDOWS%\FORMS\CONFIGS, damit das Formular automatisch wiederhergestellt werden kann, falls die Formularbibliothek beschädigt oder gelöscht wird. Dieser Schritt wird empfohlen, ist jedoch nicht zwingend erforderlich.
    
> [!NOTE]
> Sie können die Installation in einer lokalen Formularbibliothek vereinfachen, indem Sie die Schritte 1 und 2 durch einen Aufruf der [MAPIOpenLocalFormContainer-Funktion](mapiopenlocalformcontainer.md) ersetzen. 
  
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

