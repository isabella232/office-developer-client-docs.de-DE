---
title: Unterst�tzung von Formularen und Ansichten in nur-Lese Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: da5f080d-4397-4ce6-8561-73dd13445e77
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 688c0726faa5cb27f74f433e356a9931db58033f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590989"
---
# <a name="supporting-forms-and-views-in-read-only-message-stores"></a>Unterst�tzung von Formularen und Ansichten in nur-Lese Nachrichtenspeicher

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Ihre Nachricht Speicheranbieter Lesezugriff auf die zugrunde liegende Speichermechanismus zul�sst, werden kann nicht zum Ausf�hren bestimmter Vorg�nge Client-Anwendungen und der MAPI-Formular-Manager. Insbesondere Clients k�nnen keine hinzuf�gen oder �ndern benutzerdefinierte Ansichten, und der MAPI-Formular-Manager k�nnen keine Formulare in den Tabellen zugeordneten Inhalt von Ordnern f�r den Speicher zu installieren.
  
F�r viele schreibgesch�tzte Nachricht Informationsspeicher, die ein Problem m�glicherweise nicht. Wenn dies der Fall ist, muss der Nachricht Informationsdienst nicht zugeordnete Inhalt Tabellen �berhaupt zu unterst�tzen. Wenn Ihre Nachricht Speicheranbieter schreibgesch�tzt sein muss, und es muss auch eine vordefinierte Reihe von Ansichten oder Formulare unterst�tzen, m�ssen sie zur Unterst�tzung von Tabellen zugeordneten Inhalt.
  
Die am h�ufigsten verwendete Strategie zum, da dadurch Clients und der MAPI-Formular-Manager k�nnen nicht die Ansichten zu installieren oder Speichern von Formularen in die Nachricht selbst ist f�r die Nachricht Speicheranbieter vordefinierten Code sie in der Nachrichtenspeicher. Dies bedeutet, dass die zugeh�rigen Inhaltstabelle oder Tabellen, die Sichten oder -Formulare enthalten, im Nachrichtenspeicher vorhanden werden, bei der Erstellung, bevor Clients oder der MAPI-Formular-Manager jemals darauf zugreifen. Klicken Sie, wenn ein Client eine zugeordnete Inhaltstabelle zum Abrufen von benutzerdefinierter Ansichten von einem Formular fordert oder der MAPI-Formular-Manager eine zugeordnete Inhaltstabelle fordert um ein Formular zu starten, der Nachricht Store Anbieter eine bereitstellen kann. 
  
Dadurch, dass die zugeh�rigen Inhalt Tabellen erstellt und aufgef�llt, wenn der Nachrichtenspeicher selbst erstellt wird impliziert, dass Ihre Nachricht Speicheranbieter ben�tigen, Informationen zum Format der speziellen Nachrichten zu erhalten, dass Clients und der MAPI-Manager verwenden Sie zum Speichern von Datenansichten und Formularen bilden. Was sind diese Formate richtet sich nach dem Client und MAPI-Formular-Manager verwendet wird, damit eine Beschreibung f�r diese hier bereitgestellt werden kann.
  
## <a name="see-also"></a>Siehe auch



[Read-Only Nachrichtenspeicher](read-only-message-stores.md)

