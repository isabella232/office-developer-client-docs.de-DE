---
title: MAPI-Formular-Manager
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 67022a2fd85dbbc7be0dbc3f5481318f2a806d7c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592158"
---
# <a name="mapi-form-manager"></a>MAPI-Formular-Manager

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Formular-Manager ist ein Objekt, das die [IMAPIFormMgr-Schnittstelle](imapiformmgriunknown.md) implementiert. Die meisten Organisationen verwenden den mit mapi bereitgestellten Formular-Manager, der als Standardformular-Manager bezeichnet wird. Eine Organisation kann jedoch den Standardformular-Manager bei Bedarf durch einen benutzerdefinierten Formular-Manager ersetzen. Der Formular-Manager kümmert sich um die Suche nach Formularen in Formularbibliotheken, das Laden von Formularen als Reaktion auf Benutzeranforderungen und das Installieren von Formularen in der lokalen Formularbibliothek, Ordnerformularbibliothek oder persönlichen Formularbibliothek eines Benutzers. 
  
Damit ein Benutzer mit einer Nachricht interagieren kann, muss eine Instanz des Formularservers für die Nachrichtenklasse der Nachricht erstellt und aktiviert werden, um die Nachricht anzuzeigen und den angeforderten Vorgang für die Nachricht auszuführen. Wie im Thema [MAPI-Formularbibliotheken](mapi-form-libraries.md)beschrieben, kann die Implementierung eines Formulars an verschiedenen Speicherorten (Formularbibliotheken) vorhanden sein, und es gibt keine Garantie dafür, dass ein Formular oder sein Server lokal verfügbar ist oder sich in einem ausgeführten Zustand befindet, wenn ein Benutzer damit interagieren möchte. Der Formular-Manager kümmert sich um die Details der Suche und Aktivierung des Formulars.
  
Clients verwenden die vom Formular-Manager bereitgestellten Dienste, um Formulare zu suchen und zu aktivieren. Die **IMAPIFormMgr-Schnittstelle** wird vom Formular-Manager implementiert und von Clients aufgerufen, um auf ihre Dienste zuzugreifen. Der Formular-Manager ist eine wichtige Komponente, da er fast alle Details des Suchens und Aktivierens von Formularen von Messagingclients ausblendet. 
  
Beim Laden von Formularservern lädt der Standardformular-Manager das Formular aus der ersten Formularbibliothek, in der eine Implementierung für die Nachrichtenklasse des Formulars gefunden wird. Der Standardformular-Manager durchsucht die Formularbibliotheken in der folgenden Reihenfolge:
  
1. Die lokale Formularbibliothek des Benutzers. Diese Formularbibliothek wird zuerst durchsucht, da sie den schnellsten Zugriff auf die Implementierung eines Formulars bietet, wenn die Implementierung in der lokalen Formularbibliothek installiert ist.
    
2. Die Ordnerformularbibliothek des Nachrichtencontainers – der Ordner, in dem die geladene Nachricht gespeichert ist.
    
3. Die persönliche Formularbibliothek des Benutzers.
    
Ein benutzerdefinierter Formular-Manager kann die verfügbaren Formularbibliotheken in einer beliebigen Reihenfolge durchsuchen oder andere Formularbibliotheken implementieren, z. B. eine organisationsweite Formularbibliothek. Weitere Informationen zu Formularbibliotheken finden Sie unter [MAPI-Formularbibliotheken.](mapi-form-libraries.md) 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

