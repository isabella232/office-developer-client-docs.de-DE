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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351450"
---
# <a name="mapi-form-manager"></a>MAPI-Formular-Manager

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Formular-Manager ist ein Objekt, das die [IMAPIFormMgr](imapiformmgriunknown.md) -Schnittstelle implementiert. Die meisten Organisationen verwenden den mit MAPI bereitgestellten Formular-Manager, der als Standardformular-Manager bezeichnet wird. Eine Organisation kann jedoch den standardmäßigen Formular-Manager bei Bedarf durch einen benutzerdefinierten Formular-Manager ersetzen. Der Formular-Manager übernimmt die Suche nach Formularen in Formularbibliotheken, das Laden von Formularen als Reaktion auf Benutzeranfragen und das Installieren von Formularen in der lokalen Formularbibliothek eines Benutzers, in der Ordner Formularbibliothek oder in der persönlichen Formularbibliothek. 
  
Damit ein Benutzer mit einer Nachricht interagieren kann, muss eine Instanz des Formular Servers für die Nachrichtenklasse der Nachricht erstellt und aktiviert werden, um die Nachricht anzuzeigen und den angeforderten Vorgang für die Nachricht auszuführen. Wie im Thema MAPI- [Formularbibliotheken](mapi-form-libraries.md)beschrieben, kann die Implementierung eines Formulars an verschiedenen Speicherorten (Formularbibliotheken) vorhanden sein, und es gibt keine Garantie dafür, dass ein Formular oder sein Server lokal verfügbar oder in einem aktiven Zustand ist, wenn ein Benutzer interagieren möchte. . Der Formular Manager kümmert sich um die Details zum Suchen und Aktivieren des Formulars.
  
Clients verwenden vom Formular-Manager bereitgestellte Dienste zum Suchen und Aktivieren von Formularen. Die **IMAPIFormMgr** -Schnittstelle wird vom Formular-Manager implementiert und von Clients aufgerufen, um auf ihre Dienste zuzugreifen. Der Formular-Manager ist eine wesentliche Komponente, da er fast alle Details zum Suchen und Aktivieren von Formularen von Messagingclients verbirgt. 
  
Beim Laden von Formular Servern wird das Formular vom Standardformular-Manager aus der ersten Formularbibliothek geladen, in der eine Implementierung für die Nachrichtenklasse des Formulars gefunden wird. Der Standardformular-Manager durchsucht die Formularbibliotheken in der folgenden Reihenfolge:
  
1. Die lokale Formularbibliothek des Benutzers. Diese Formularbibliothek wird zuerst durchsucht, da Sie den schnellsten Zugriff auf die Implementierung eines Formulars ermöglicht, wenn die Implementierung in der lokalen Formularbibliothek installiert ist.
    
2. Die Ordner Formularbibliothek des Containers der Nachricht – der Ordner, in dem die zu ladende Nachricht gespeichert wird.
    
3. Die persönliche Formularbibliothek des Benutzers.
    
Ein benutzerdefinierter Formular-Manager kann die verfügbaren Formularbibliotheken in beliebiger Reihenfolge durchsuchen oder andere Formularbibliotheken wie eine organisationsweite Formularbibliothek implementieren. Weitere Informationen zu Formularbibliotheken finden Sie unter [MAPI-Formularbibliotheken](mapi-form-libraries.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

