---
title: Informationen zu Besprechungsanfragen als informative und vollständige Aktualisierungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 084928ca-efc0-36da-fe4f-5cc45f226178
description: Eine Besprechungsanfrage ist eine E-Mail mit IPM. Schedule.Meeting.Request als Nachrichtenklasse. Standardmäßig antwortet ein Teilnehmer, der eine Besprechungsanfrage empfängt, direkt darauf.
ms.openlocfilehash: d6e138fb4639a590e31e5f797ff3604c050c6292
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605470"
---
# <a name="about-meeting-requests-as-informational-updates-and-full-updates"></a>Informationen zu Besprechungsanfragen als informative und vollständige Aktualisierungen

Eine Besprechungsanfrage ist eine E-Mail mit **IPM. Schedule.Meeting.Request** als Nachrichtenklasse. Standardmäßig antwortet ein Teilnehmer, der eine Besprechungsanfrage empfängt, direkt darauf. Outlook unterstützt das Einrichten von Stellvertretungen, die im Auftrag des Hauptempfängers auf Besprechungsanfragen antworten können. Programmgesteuert legt Outlook die benannte Eigenschaft [PidLidMeetingType](https://msdn.microsoft.com/library/290b290c-7836-4a7e-bf1a-8d0225a07e56%28Office.15%29.aspx) einer Besprechungsanfrage fest, um den aktuellen Aktualisierungsstatus zu identifizieren. 
  
## <a name="recipients-without-delegates"></a>Empfänger ohne Stellvertretungen

Wenn Outlook eine neue Besprechungsanfrage erhält, legt Outlook die **PidLidMeetingType-Eigenschaft** des Besprechungsanfrageelements auf **mtgRequest** fest. Jedes nachfolgende Update dieser Besprechung ist entweder **mtgFullUpdate** (ein vollständiges Update) oder **mtgInfoUpdate** (ein Informationsupdate) je nach Ursache des Updates, wobei Outlook **PidLidMeetingType** entsprechend festlegen. Ein vollständiges Update erfordert, dass ein Teilnehmer explizit auf die Besprechungsanfrage antwortet, und ein Informationsupdate ist dies nicht. 
  
## <a name="full-updates"></a>Vollständige Updates

Es gibt zwei Szenarien, die zu einer vollständigen Aktualisierung führen:
  
- Wenn ein Organisator das Datum, die Uhrzeit, die Zeitzonen oder die Wiederholung einer vorherigen Besprechungsanfrage ändert, muss der Organisator eine Aktualisierung an alle Teilnehmer senden. Dieses Update ist ein vollständiges Update, auf das ein Teilnehmer explizit reagieren muss, um den Organisator über die Teilnahme zu benachrichtigen, da Outlook alle vorherigen Antworten ignoriert.
    
- Wenn ein Teilnehmer auf eine anfängliche Besprechungsanfrage nicht geantwortet hat und ein nachfolgendes Update erhält, wird die ursprüngliche Besprechungsanfrage veraltet und das Update ist ein vollständiges Update, unabhängig von der Ursache des Updates.
    
## <a name="informational-updates"></a>Informationsupdates

Es gibt vier Szenarien, in denen Outlook ein Informationsupdate generiert. In diesen Szenarien ist die Reaktion auf das Informationsupdate optional.
  
- Wenn ein Organisator den Ort einer vorherigen Besprechungsanfrage ändert, muss der Organisator eine Aktualisierung an alle Teilnehmer senden. Wenn ein Teilnehmer die ursprüngliche Besprechungsanfrage bereits angenommen hat, erhält der Teilnehmer das Update als Informationsupdate.
    
- Wenn ein Organisator einen Teilnehmer zu einer vorherigen Besprechungsanfrage hinzufügt, muss der Organisator die Besprechungsanfrage an den neu hinzugefügten Teilnehmer senden und hat die Möglichkeit, vorhandene Teilnehmer in das Update einzuschließen. Der neu hinzugefügte Teilnehmer empfängt die Besprechungsanfrage als neue Anforderung. Wenn der Organisator ein Update an vorhandene Teilnehmer sendet, erhalten die Teilnehmer das Update als Informationsupdate.
    
- Wenn ein Organisator einen Teilnehmer aus einer vorherigen Besprechungsanfrage entfernt, muss der Organisator eine Aktualisierung an den Teilnehmer senden, der aus der Besprechungsanfrage entfernt wurde, und hat die Möglichkeit, vorhandene Teilnehmer in das Update einzuschließen. Teilnehmer erhalten das Update als Informationsupdate.
    
- Wenn ein Organisator den Betreff oder den Textkörper einer vorherigen Besprechungsanfrage ändert, hat der Organisator die Möglichkeit, eine Aktualisierung an die Teilnehmer zu senden oder die Änderungen einfach in der kopie der Besprechungsanfrage des Organisators zu speichern. Wenn der Organisator ein Update sendet, erhalten die Teilnehmer das Update als Informationsupdate.
    
## <a name="recipients-set-up-with-delegates"></a>Mit Stellvertretungen eingerichtete Empfänger

Empfänger, die Stellvertretungen einrichten möchten, können Stellvertretungen auf Besprechungsanfragen antworten lassen, die nicht als "Privat" gekennzeichnet sind. Standardmäßig empfängt der Prinzipal nur eine Kopie einer Besprechungsanfrage oder eine Kopie einer Aktualisierung einer vorherigen Besprechungsanfrage, und die Stellvertreter erhalten immer die ursprüngliche Besprechungsanfrage oder die ursprüngliche vollständige oder informationsbezogene Aktualisierung. In dieser Standardkonfiguration empfängt der Prinzipal immer delegierte Besprechungsanfragen und Updates; Stellvertreter des Prinzipals empfangen Besprechungsanfragen als neue Besprechungsanfragen, vollständige Aktualisierungen oder Informationsupdates, wie für Empfänger ohne Stellvertreter im Abschnitt "Empfänger ohne Stellvertreter" beschrieben.
  
Standardmäßig können Prinzipale entscheiden, auf nicht private Besprechungsanfragen und -aktualisierungen zu reagieren, obwohl Stellvertretungen dafür in ihrem Auftrag eingerichtet sind. Alternativ können Administratoren jedoch eine Richtlinie einrichten, um zu verhindern, dass Hauptempfänger antworten.
  

