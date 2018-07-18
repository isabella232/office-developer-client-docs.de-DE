---
title: MAPI-Formular-Manager
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d12d879ea5a82c5e0e3978d90694b3851aaac5cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792983"
---
# <a name="mapi-form-manager"></a>MAPI-Formular-Manager

  
  
**Betrifft**: Outlook 
  
Ein Formular-Manager ist ein Objekt, das die [IMAPIFormMgr](imapiformmgriunknown.md) -Schnittstelle implementiert wird. Die meisten Organisationen verwenden den Formular-Manager Lieferumfang MAPI, als der Standard-Formular-Manager bezeichnet. Jedoch kann eine Organisation den Standard-Formular-Manager mit einem benutzerdefinierten Formular-Manager ersetzen, falls gewünscht. Der Formular-Manager kümmert Auffinden von Formularen in Formularbibliotheken, Laden von Formularen in Reaktion auf Benutzeranfragen und Formulare in lokalen Formularbibliothek, Ordner-Formularbibliothek oder persönliche Formularbibliothek des Benutzers installieren. 
  
Für einen Benutzer für die Interaktion mit einer Meldung muss eine Instanz des Servers für die Nachricht Nachrichtenklasse Formular erstellt und aktiviert, um die Meldung angezeigt, und führen Sie den angeforderten Vorgang für die Nachricht. Wie im Thema [MAPI Formularbibliotheken](mapi-form-libraries.md)beschrieben, kann Implementierung eines Formulars an unterschiedlichen Speicherorten (Formularbibliotheken) vorhanden und kann nicht garantiert, dass ein Formular oder der entsprechende Server lokal verfügbar sein oder in einer laufenden, wenn Benutzer angeben für die Interaktion wird mit diesem. Der Formular-Manager sorgt für ausführliche Informationen zu suchen und aktivieren das Formular.
  
Clients verwenden von der Formular-Manager bereitgestellten Dienste zum Suchen und Aktivieren von Formularen. Die **IMAPIFormMgr** -Schnittstelle wird von der Formular-Manager implementiert und von Clients für den Zugriff auf seine Services aufgerufen wird. Der Formular-Manager ist ein wesentlicher Bestandteil, da es fast alle Details der suchen und Aktivieren von Formularen von messaging-Clients werden ausgeblendet. 
  
Formular Servern zu laden, lädt der Standard-Formular-Manager das Formular aus der ersten Formularbibliothek, in der Sie eine Implementierung für die Nachrichtenklasse des Formulars befindet. Der Standard-Formular-Manager sucht die Formularbibliotheken in der folgenden Reihenfolge:
  
1. Lokale Formularbibliothek des Benutzers. Diese Formularbibliothek wird zuerst durchsucht, da es den schnellsten Zugriff auf die Implementierung eines Formulars bereitstellt, wenn die Implementierung in der lokalen Formularbibliothek installiert ist.
    
2. Der Ordner-Formularbibliothek die Nachricht Containers – der Ordner, in dem die Nachricht geladene gespeichert ist.
    
3. Der Benutzer Persönliche Formularbibliothek.
    
Ein benutzerdefiniertes Formular-Manager kann die verfügbaren Formularbibliotheken in beliebiger Reihenfolge suchen oder anderen Formularbibliotheken wie etwa einer Organisation geltende Formularbibliothek implementieren kann. Weitere Informationen zu Formularbibliotheken finden Sie unter [MAPI Formularbibliotheken](mapi-form-libraries.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

