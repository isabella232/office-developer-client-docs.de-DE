---
title: MAPI-Formular-Manager
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3059183103ca2552505486b5ec54366729ae4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430196"
---
# <a name="mapi-form-manager"></a>MAPI-Formular-Manager

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Formular-Manager ist ein Objekt, das die [IMAPIFormMgr-Schnittstelle](imapiformmgriunknown.md) implementiert. Die meisten Organisationen verwenden den mit MAPI bereitgestellten Formular-Manager, der als Standardformular-Manager bezeichnet wird. Eine Organisation kann jedoch bei Bedarf den Standardformular-Manager durch einen benutzerdefinierten Formular-Manager ersetzen. Der Formular-Manager kümmert sich um das Suchen von Formularen in Formularbibliotheken, das Laden von Formularen als Reaktion auf Benutzeranforderungen und das Installieren von Formularen in der lokalen Formularbibliothek, der Ordnerformularbibliothek oder der persönlichen Formularbibliothek eines Benutzers. 
  
Damit ein Benutzer mit einer Nachricht interagieren kann, muss eine Instanz des Formularservers für die Nachrichtenklasse der Nachricht erstellt und aktiviert werden, um die Nachricht anzeigen und den angeforderten Vorgang für die Nachricht durchführen zu können. Wie im Thema [MAPI-Formularbibliotheken](mapi-form-libraries.md)beschrieben, kann die Implementierung eines Formulars an mehreren verschiedenen Speicherorten (Formularbibliotheken) vorhanden sein, und es gibt keine Garantie, dass ein Formular oder sein Server lokal verfügbar ist oder sich in einem ausgeführten Zustand befindet, wenn ein Benutzer mit ihm interagieren möchte. Der Formularmanager kümmert sich um die Details des Suchens und Aktivierens des Formulars.
  
Clients verwenden Dienste, die vom Formular-Manager bereitgestellt werden, um Formulare zu finden und zu aktivieren. Die **IMAPIFormMgr-Schnittstelle** wird vom Formular-Manager implementiert und von Clients aufgerufen, um auf die Dienste zu zugreifen. Der Formular-Manager ist eine wesentliche Komponente, da er fast alle Details zum Suchen und Aktivieren von Formularen in Messagingclients ausblendet. 
  
Beim Laden von Formularservern lädt der Standardformular-Manager das Formular aus der ersten Formularbibliothek, in der eine Implementierung für die Nachrichtenklasse des Formulars gefunden wird. Der Standardformular-Manager durchsucht die Formularbibliotheken in der folgenden Reihenfolge:
  
1. Die lokale Formularbibliothek des Benutzers. Diese Formularbibliothek wird zuerst durchsucht, da sie den schnellsten Zugriff auf die Implementierung eines Formulars bietet, wenn die Implementierung in der lokalen Formularbibliothek installiert ist.
    
2. Die Ordnerformularbibliothek des Nachrichtencontainers – der Ordner, in dem die zu ladende Nachricht gespeichert wird.
    
3. Die persönliche Formularbibliothek des Benutzers.
    
Ein benutzerdefinierter Formular-Manager kann die verfügbaren Formularbibliotheken in beliebiger Reihenfolge durchsuchen oder andere Formularbibliotheken implementieren, z. B. eine organisationsweite Formularbibliothek. Weitere Informationen zu Formularbibliotheken finden Sie unter [MAPI Form Libraries](mapi-form-libraries.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

