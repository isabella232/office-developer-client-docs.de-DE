---
title: Informationen zu Besprechungsanfragen als informative und vollständige Aktualisierungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 084928ca-efc0-36da-fe4f-5cc45f226178
description: Eine Besprechungsanfrage ist eine e-Mail mit IPM. Schedule. Meeting. Request als Nachrichtenklasse. Standardmäßig antwortet ein Teilnehmer, der eine Besprechungsanfrage erhält, direkt darauf.
ms.openlocfilehash: 8e7ab7a85d3f9f7c0a67245b8d8ad27442f5c5e4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316996"
---
# <a name="about-meeting-requests-as-informational-updates-and-full-updates"></a>Informationen zu Besprechungsanfragen als informative und vollständige Aktualisierungen

Eine Besprechungsanfrage ist eine e-Mail mit **IPM. Schedule. Meeting. Request** als Nachrichtenklasse. Standardmäßig antwortet ein Teilnehmer, der eine Besprechungsanfrage erhält, direkt darauf. Outlook unterstützt das Einrichten von Stellvertretungen, die im Namen des Hauptempfängers auf Besprechungsanfragen Antworten können. In Outlook wird die benannte Eigenschaft [pidlidmeetingtype (](https://msdn.microsoft.com/library/290b290c-7836-4a7e-bf1a-8d0225a07e56%28Office.15%29.aspx) einer Besprechungsanfrage programmgesteuert festgelegt, um den aktuellen Updatestatus zu identifizieren. 
  
## <a name="recipients-without-delegates"></a>Empfänger ohne Stellvertreter

Wenn Outlook eine neue Besprechungsanfrage erhält, wird die **pidlidmeetingtype (** -Eigenschaft des Besprechungs Anforderungs Elements auf **mtgRequest**festgelegt. Jede nachfolgende Aktualisierung dieser Besprechung ist entweder **mtgFullUpdate** (ein vollständiges Update) oder **mtgInfoUpdate** (ein Informations Update) abhängig von der Ursache des Updates, wobei die Outlook-Einstellung **pidlidmeetingtype (** entsprechend ist. Eine vollständige Aktualisierung erfordert, dass ein Teilnehmer explizit auf die Besprechungsanfrage antwortet und eine Informationsaktualisierung nicht. 
  
## <a name="full-updates"></a>Vollständige Updates

Es gibt zwei Szenarien, die zu einer vollständigen Aktualisierung führen:
  
- Wenn ein Organisator das Datum, die Uhrzeit, die Zeitzonen oder die Wiederholung einer früheren Besprechungsanfrage ändert, muss der Organisator eine Aktualisierung an alle Teilnehmer senden. Bei diesem Update handelt es sich um eine vollständige Aktualisierung, auf die ein Teilnehmer explizit Antworten muss, um den Organisator der Anwesenheit zu benachrichtigen, da Outlook frühere Antworten ignoriert.
    
- Wenn ein Teilnehmer nicht auf eine anfängliche Besprechungsanfrage geantwortet hat und ein nachfolgendes Update erhält, wird die anfängliche Besprechungsanfrage veraltet, und das Update ist unabhängig von der Ursache des Updates ein vollständiges Update.
    
## <a name="informational-updates"></a>Informationsaktualisierungen

Es gibt vier Szenarios, in denen Outlook ein Informations Update generiert. In diesen Szenarien ist die Reaktion auf das Informations Update optional.
  
- Wenn ein Organisator den Speicherort einer früheren Besprechungsanfrage ändert, muss der Organisator eine Aktualisierung an alle Teilnehmer senden. Wenn ein Teilnehmer die anfängliche Besprechungsanfrage bereits akzeptiert hat, erhält der Teilnehmer das Update als Informations Update.
    
- Wenn ein Organisator einer früheren Besprechungsanfrage einen Teilnehmer hinzufügt, muss der Organisator die Besprechungsanfrage an den neu hinzugefügten Teilnehmer senden und kann vorhandene Teilnehmer in das Update einbeziehen. Der neu hinzugefügte Teilnehmer erhält die Besprechungsanfrage als neue Anforderung. Wenn der Organisator eine Aktualisierung an vorhandene Teilnehmer sendet, erhalten die Teilnehmer das Update als Informations Update.
    
- Wenn ein Organisator einen Teilnehmer aus einer früheren Besprechungsanfrage entfernt, muss der Organisator eine Aktualisierung an den Teilnehmer senden, der aus der Besprechungsanfrage entfernt wurde und eine Option zum Einbeziehen vorhandener Teilnehmer in das Update hat. Teilnehmer erhalten das Update als Informations Update.
    
- Wenn ein Organisator den Betreff oder den Text einer früheren Besprechungsanfrage ändert, hat der Organisator die Möglichkeit, eine Aktualisierung an die Teilnehmer zu senden oder die Änderungen einfach in der eigenen Kopie der Besprechungsanfrage des Organisators zu speichern. Wenn der Organisator ein Update sendet, erhalten die Teilnehmer das Update als Informations Update.
    
## <a name="recipients-set-up-with-delegates"></a>Mit Stellvertretungen eingerichteten Empfängern

Empfänger, die Delegaten einrichten möchten, können auf Besprechungsanfragen Antworten, die nicht als privat gekennzeichnet sind. Standardmäßig erhält der Prinzipal nur eine Kopie einer Besprechungsanfrage oder eine Kopie eines Updates an eine vorherige Besprechungsanfrage, und die Stellvertreter erhalten immer die ursprüngliche Besprechungsanfrage oder das ursprüngliche vollständige oder inständige Update. In dieser Standardkonfiguration erhält der Prinzipal immer Delegierte Besprechungsanfragen und Aktualisierungen; Delegaten des Prinzipals empfangen Besprechungsanfragen als neue Besprechungsanfragen, vollständige Updates oder Informationsaktualisierungen, wie für Empfänger ohne Stellvertreter im Abschnitt "Empfänger ohne Stellvertreter" beschrieben.
  
Standardmäßig können Prinzipale auf nicht-private Besprechungsanfragen und-Updates Antworten, auch wenn die Stellvertretungen dafür in Ihrem Namen eingerichtet sind. Alternativ können Administratoren jedoch eine Richtlinie einrichten, um zu verhindern, dass Prinzipal Empfänger reagieren.
  

