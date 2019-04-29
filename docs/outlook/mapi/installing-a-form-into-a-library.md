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
  
Der standardmäßige MAPI-Formular-Manager, der mit dem Windows SDK bereitgestellt wird, bietet keine Benutzeroberfläche für die Installation von Formularen in den verschiedenen Formularbibliotheken. Aus diesem Grund müssen Sie eine kleine Anwendung oder detaillierte Anweisungen erstellen, mit denen Benutzer das Formular installieren können.
  
Wenn Sie eine Installationsanwendung implementieren, müssen die folgenden Aktionen ausgeführt werden, um ein Formular in der Tabelle mit den zugeordneten Inhalten eines Ordners zu installieren:
  
1. Rufen Sie die [MAPIOpenFormMgr](mapiopenformmgr.md) -Funktion auf, um den Formular-Manager zu öffnen. 
    
2. Verwenden Sie [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) oder [IMAPIFormMgr:: SelectFormContainer](imapiformmgr-selectformcontainer.md) -Methode, um den Zielcontainer für das Formular auszuwählen und zu öffnen. 
    
3. Verwenden Sie die [IMAPIFormContainer:: InstallForm](imapiformcontainer-installform.md) -Funktion, um das Formular zu installieren. 
    
    Die Schritte 4 bis 6 sind für die Installation in einer lokalen Formularbibliothek erforderlich:
    
4. Kopieren Sie alle Dateien an den entsprechenden Speicherort auf dem lokalen Datenträger, wenn die Installation in der lokalen Formularbibliothek auf der Arbeitsstation des Benutzers erfolgt. Ändern Sie bei Bedarf die Formular Konfigurationsdatei entsprechend den aktuellen Pfaden von Komponenten. Die Formular Konfigurationsdatei kann relative Pfade enthalten, in diesem Fall ist dieser Schritt möglicherweise nicht erforderlich.
    
5. Führen Sie die entsprechenden OLE-Registrierungsschritte aus, um den Nachrichtentyp dem installierten Formularserver zuzuordnen.
    
6. Wenn das Formular in der lokalen Formularbibliothek installiert wurde, kopieren Sie das Formularsymbol (ICO) und die Konfigurationsdateien (. cfg) in das Verzeichnis%WINDOWS%\FORMS\CONFIGS, damit das Formular automatisch wiederhergestellt werden kann, falls die Formularbibliothek beschädigt oder gelöscht wird. Dieser Schritt wird empfohlen, aber nicht zwingend erforderlich.
    
> [!NOTE]
> Sie können die Installation in einer lokalen Formularbibliothek vereinfachen, indem Sie die Schritte 1 und 2 durch einen Aufruf der [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) -Funktion ersetzen. 
  
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formular Servern](developing-mapi-form-servers.md)

