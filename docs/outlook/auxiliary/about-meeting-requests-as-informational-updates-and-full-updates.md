---
title: Informationen zu Besprechungsanfragen als Informationszwecken und vollständige updates
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 084928ca-efc0-36da-fe4f-5cc45f226178
description: Eine Besprechungsanfrage wird eine e-Mail-Nachricht, die IPM hat. Schedule.Meeting.Request als die Nachrichtenklasse. Standardmäßig antwortet Teilnehmerin annehmen einer Besprechungsanfrage von direkt hinzu.
ms.openlocfilehash: 3565b2af03ef79d70fc9f2817c64a788f031c416
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790922"
---
# <a name="about-meeting-requests-as-informational-updates-and-full-updates"></a>Informationen zu Besprechungsanfragen als Informationszwecken und vollständige updates

Eine Besprechungsanfrage wird eine e-Mail-Nachricht, die **IPM hat. Schedule.Meeting.Request** als die Nachrichtenklasse. Standardmäßig antwortet Teilnehmerin annehmen einer Besprechungsanfrage von direkt hinzu. Outlook unterstützt einrichten Stellvertretungen, die auf Besprechungsanfragen im Namen der principal-Empfänger Antworten können. Programmgesteuertes, aktiviert Outlook die benannte Eigenschaft [PidLidMeetingType](http://msdn.microsoft.com/library/290b290c-7836-4a7e-bf1a-8d0225a07e56%28Office.15%29.aspx) einer Besprechungsanfrage, um den aktuellen Status zu identifizieren. 
  
## <a name="recipients-without-delegates"></a>Empfänger, die nicht von Stellvertretungen

Wenn Outlook eine neue Besprechungsanfrage Outlook legt die **PidLidMeetingType** -Eigenschaft der Besprechungsanfrage zu **MtgRequest**Element empfängt. Nachfolgende Updates diese Besprechung ist **MtgFullUpdate** (eine vollständige Aktualisierung) oder **MtgInfoUpdate** (Informationszwecken Update) je nach Ursache des Updates mit Outlook **PidLidMeetingType** entsprechend festlegen. Eine vollständige Aktualisierung erfordert einen Teilnehmer explizit Antworten auf die Besprechungsanfrage, und nicht der Fall ist ein Informationszwecken Update. 
  
## <a name="full-updates"></a>Vollständige updates

Es gibt zwei Szenarien, die eine vollständige Aktualisierung führen:
  
- Wenn das Datum, Uhrzeit, Zeitzonen oder Serie von einer vorherigen Besprechungsanfrage Organisator geändert wird, muss der Organisator eine Aktualisierung an alle Teilnehmer senden. Dieses Update ist eine vollständige Aktualisierung auf die Teilnehmerin explizit reagieren muss, um dem Organisator des Anwesenheit, benachrichtigen, da Outlook alle vorherigen Antworten ignoriert.
    
- Wenn ein Teilnehmer nicht auf eine anfängliche Besprechungsanfrage geantwortet hat und eine nachfolgende Aktualisierung erhält, die ursprüngliche Besprechungsanfrage ist veraltet und das Update ist eine vollständige Aktualisierung, unabhängig von der Ursache des Updates.
    
## <a name="informational-updates"></a>Informative updates

Es gibt vier Szenarien, die in denen Outlook ein Informationszwecken Update erstellt wird. In diesen Szenarien ist die Reaktion auf das Update Informationszwecken optional.
  
- Wenn der Organisator den Speicherort einer vorherigen Besprechungsanfrage geändert wird, muss der Organisator eine Aktualisierung an alle Teilnehmer senden. Wenn ein Teilnehmer bereits die ursprüngliche Besprechungsanfrage angenommen, erhält der Teilnehmer das Update als Informationszwecken Update.
    
- Wenn Organisator ein Teilnehmers auf eine vorherige Besprechungsanfrage hinzufügt, der Organisator muss die Besprechungsanfrage an den neu hinzugefügten Teilnehmer senden und hat die Option zum Einschließen von vorhandenen Teilnehmer auf das Update. Der neu hinzugefügte Teilnehmer erhält die Besprechungsanfrage als neue Anforderung. Wenn der Organisator ein Update auf vorhandene Teilnehmer senden möchte, empfangen die Teilnehmer das Update als Informationszwecken Update.
    
- Wenn einen Teilnehmer aus einer früheren Besprechungsanfrage Organisator entfernt werden, muss der Organisator ein Update der Teilnehmer senden, die wurde aus der Besprechungsanfrage entfernt und verfügt über die Option vorhandene Teilnehmer auf das Update enthalten. Teilnehmer erhalten die Aktualisierung als Informationszwecken Update.
    
- Wenn der Organisator der Betreff oder Textkörper des eine vorherige Besprechungsanfrage geändert wird, hat der Organisator die Möglichkeit, eine Aktualisierung an die Teilnehmer senden oder nur die Änderungen auf die Kopie des Organisators der Besprechungsanfrage zu speichern. Wenn der Organisator entscheidet, eine Aktualisierung zu senden, die Aktualisierung von Teilnehmern als Informationszwecken Update erhalten.
    
## <a name="recipients-set-up-with-delegates"></a>Empfänger mit Stellvertretungen eingerichtet

Empfänger, die Stellvertretungen einrichten können Delegaten Antworten auf Besprechungsanfragen, die nicht privat gekennzeichnet sind. Standardmäßig der Prinzipal empfängt nur eine Kopie einer Besprechungsanfrage oder eine Kopie eines Updates auf eine vorherige Besprechungsanfrage, und die Delegaten empfangen immer die ursprüngliche Besprechungsanfrage oder ursprüngliche vollständige oder informative Update. In dieser Standardkonfiguration erhält der Prinzipal immer delegierte Besprechungsanfragen und Updates. Stellvertretungen des Prinzipals empfangen Besprechungsanfragen als neue Besprechungsanfragen, vollständige Updates oder Informationszwecken Updates gemäß für Empfänger ohne Delegaten im Abschnitt "Empfänger ohne Stellvertretungen".
  
Prinzipale können standardmäßig auf privaten Besprechungsanfragen und Aktualisierungsvorgänge, reagieren, obwohl die Stellvertretungen eingerichtet sind, die in ihrem Auftrag ausführen. Jedoch können als Alternative Administratoren eine Richtlinie so einrichten reagiert principal Empfänger zu verhindern.
  

