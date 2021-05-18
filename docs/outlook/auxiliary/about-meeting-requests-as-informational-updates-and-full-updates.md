---
title: Informationen zu Besprechungsanfragen als informative und vollständige Aktualisierungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 084928ca-efc0-36da-fe4f-5cc45f226178
description: Eine Besprechungsanfrage ist eine E-Mail mit IPM. Schedule.Meeting.Request als Nachrichtenklasse. Standardmäßig antwortet ein Teilnehmer, der eine Besprechungsanfrage empfängt, direkt darauf.
ms.openlocfilehash: 8e7ab7a85d3f9f7c0a67245b8d8ad27442f5c5e4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316996"
---
# <a name="about-meeting-requests-as-informational-updates-and-full-updates"></a>Informationen zu Besprechungsanfragen als informative und vollständige Aktualisierungen

Eine Besprechungsanfrage ist eine E-Mail mit **IPM. Schedule.Meeting.Request** als Nachrichtenklasse. Standardmäßig antwortet ein Teilnehmer, der eine Besprechungsanfrage empfängt, direkt darauf. Outlook unterstützt das Einrichten von Stellvertretungsvertretern, die auf Besprechungsanfragen im Namen des Hauptempfängers reagieren können. Programmgesteuert legt Outlook die benannte Eigenschaft [PidLidMeetingType](https://msdn.microsoft.com/library/290b290c-7836-4a7e-bf1a-8d0225a07e56%28Office.15%29.aspx) einer Besprechungsanfrage fest, um den aktuellen Aktualisierungsstatus zu identifizieren. 
  
## <a name="recipients-without-delegates"></a>Empfänger ohne Stellvertreter

Wenn Outlook eine neue Besprechungsanfrage empfängt, legt Outlook **die PidLidMeetingType-Eigenschaft** des Besprechungsanforderungselements auf **mtgRequest fest.** Jedes nachfolgende Update dieser Besprechung ist entweder **mtgFullUpdate** (ein vollständiges Update) oder **mtgInfoUpdate** (ein Informationsupdate), je nach Ursache des Updates, und Outlook **PidLidMeetingType** entsprechend festlegen. Bei einer vollständigen Aktualisierung muss ein Teilnehmer explizit auf die Besprechungsanfrage antworten, und ein Informationsupdate ist nicht erforderlich. 
  
## <a name="full-updates"></a>Vollständige Updates

Es gibt zwei Szenarien, die zu einer vollständigen Aktualisierung führen:
  
- Wenn ein Organisator Datum, Uhrzeit, Zeitzonen oder Serien einer vorherigen Besprechungsanfrage ändert, muss der Organisator ein Update an alle Teilnehmer senden. Dieses Update ist ein vollständiges Update, auf das ein Teilnehmer explizit reagieren muss, um den Organisator über die Teilnahme zu benachrichtigen, da Outlook vorherige Antworten ignoriert.
    
- Wenn ein Teilnehmer nicht auf eine anfängliche Besprechungsanfrage geantwortet hat und ein nachfolgendes Update erhält, ist die anfängliche Besprechungsanfrage veraltet, und das Update ist ein vollständiges Update, unabhängig von der Ursache des Updates.
    
## <a name="informational-updates"></a>Informationsupdates

Es gibt vier Szenarien, in denen Outlook ein Informationsupdate generiert. In diesen Szenarien ist die Reaktion auf das Informationsupdate optional.
  
- Wenn ein Organisator den Speicherort einer vorherigen Besprechungsanfrage ändert, muss der Organisator ein Update an alle Teilnehmer senden. Wenn ein Teilnehmer die ursprüngliche Besprechungsanfrage bereits akzeptiert hat, erhält der Teilnehmer das Update als Informationsupdate.
    
- Wenn ein Organisator einen Teilnehmer zu einer vorherigen Besprechungsanfrage hinzufügt, muss der Organisator die Besprechungsanfrage an den neu hinzugefügten Teilnehmer senden und hat die Möglichkeit, vorhandene Teilnehmer in das Update zu verwenden. Der neu hinzugefügte Teilnehmer empfängt die Besprechungsanfrage als neue Anforderung. Wenn der Organisator ein Update an vorhandene Teilnehmer sendet, erhalten die Teilnehmer das Update als Informationsupdate.
    
- Wenn ein Organisator einen Teilnehmer aus einer vorherigen Besprechungsanfrage entfernt, muss der Organisator ein Update an den Teilnehmer senden, der aus der Besprechungsanfrage entfernt wurde und über eine Option zum Hinzufügen vorhandener Teilnehmer in das Update verfügt. Teilnehmer erhalten das Update als Informationsupdate.
    
- Wenn ein Organisator den Betreff oder Text einer vorherigen Besprechungsanfrage ändert, hat der Organisator die Möglichkeit, ein Update an die Teilnehmer zu senden oder die Änderungen einfach in der eigenen Kopie der Besprechungsanfrage des Organisators zu speichern. Wenn der Organisator ein Update sendet, erhalten die Teilnehmer das Update als Informationsupdate.
    
## <a name="recipients-set-up-with-delegates"></a>Empfänger, die mit Stellvertretern eingerichtet wurden

Empfänger, die Stellvertretung einrichten, können Stellvertretung auf Besprechungsanfragen reagieren lassen, die nicht als Privat gekennzeichnet sind. Standardmäßig erhält der Prinzipal nur eine Kopie einer Besprechungsanfrage oder eine Kopie einer Aktualisierung einer vorherigen Besprechungsanfrage, und die Stellvertretung erhält immer die ursprüngliche Besprechungsanfrage oder das ursprüngliche vollständige oder informationelle Update. In dieser Standardkonfiguration empfängt der Prinzipal immer delegierte Besprechungsanfragen und -updates. Stellvertretung des Prinzipals empfangen Besprechungsanfragen als neue Besprechungsanfragen, vollständige Updates oder Informationsupdates, wie für Empfänger ohne Stellvertreter im Abschnitt "Empfänger ohne Stellvertreter" beschrieben.
  
Prinzipale können standardmäßig auf nicht private Besprechungsanfragen und -updates reagieren, auch wenn Stellvertretungsvertreter dafür in ihrem Auftrag eingerichtet sind. Alternativ können Administratoren jedoch eine Richtlinie einrichten, um zu verhindern, dass Prinzipalempfänger reagieren.
  

