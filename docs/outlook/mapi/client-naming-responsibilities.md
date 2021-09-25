---
title: Clientbenennungsaufgaben
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: dbb6ba5f-18c8-426f-9f50-ce6f2fd1dc5b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: de707abc99393d40461e0f2be696040b570764d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584689"
---
# <a name="client-naming-responsibilities"></a>Clientbenennungsaufgaben

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients müssen eine Benennungskonvention für ihre Eigenschaften befolgen, die von einem Gateway übersetzt werden müssen. Alle zu übersetzenden Eigenschaften sollten als benannte Eigenschaften in einem der fünf Eigenschaftensätze erstellt werden, die zugeordnete Eigenschaften enthalten sollen:
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_ROUTING_SEARCH_KEY
  
Die Adressierung von Eigenschaften, die sich auf denselben Benutzer beziehen, muss denselben Namen erhalten. Gateways basieren auf dieser Benennungskonvention, die es ihnen ermöglicht, eine Adresse mit ihrem richtigen Adresstyp abzugleichen. Für die Adressanalyse muss die Zuordnung zwischen Adresse und Adresstyp korrekt sein.
  
BENANNTE MAPI-Eigenschaften werden mit der **MAPINAMEID-Datenstruktur** dargestellt, die angibt, dass der Eigenschaftenname entweder eine Unicode-Zeichenfolge oder eine 32-Bit-Ganzzahl sein kann. Weitere Informationen finden Sie unter [MAPINAMEID.](mapinameid.md) Die Ganzzahlbenennung wird für Adressgruppen empfohlen, da es eine einfache Möglichkeit ist, zwischen Sätzen von zuordbaren Eigenschaften zu unterscheiden, und sie kann dem Benutzer leicht als Index dienen. Die Alternative zur Verwendung von ganzzahligen Zahlen besteht darin, eine Zeichenfolge als Namen für alle fünf zuordbaren Eigenschaften eines Benutzers zuzuweisen. Wenn nur ein Benutzer eine Zuordnung erfordert, ist das Zuweisen einer Zeichenfolge zulässig. Wenn jedoch mehrere Benutzer vorhanden sind, ist es besser, ganzzahlige Benennungen zu verwenden. Der Name, ganz gleich, ob numerisch oder zeichenfolgenbasiert, sollte entweder in einer nachrichtenklassenspezifischen Eigenschaft oder in einer Eigenschaft gespeichert werden, die zu einem Von der Clientanwendung definierten Eigenschaftensatz gehört. 
  
> [!NOTE]
> Vermeiden Sie die Übersetzung ganzzahliger Namen in Zeichenfolgen, z. B. "route_recipient_1" und "route_recipient_2". Dieser Aufwand ist unnötig. 
  
Um zu veranschaulichen, wie diese Benennungskonvention funktioniert, ziehen Sie eine Routinganwendung in Betracht, die eine Nachricht an jedes Mitglied eines vierseitigen Teams sendet. Wenn ein Mitglied die Nachricht empfängt, muss es darauf antworten, bevor es zusammen mit den kompilierten Antworten an das nächste Mitglied gesendet werden kann. Die ursprüngliche Nachricht enthält eine Empfängerliste mit einem Eintrag: dem ersten Mitglied des Teams. Eingebettet in die Nachricht sind die gatewayzuordnungsfähigen Eigenschaften für die anderen drei Teammitglieder. Jedes Mitglied verfügt über fünf Hauptbenutzereigenschaften, die sich in den gatewayzuordnungsfähigen Eigenschaftensätzen befinden, denen eine eindeutige Nummer als Name zugewiesen wird. 
  
In der folgenden Tabelle sind die Einstellungen für jeden Satz von gatewayzuordnungsfähigen Eigenschaften dargestellt, die für die drei verbleibenden Teammitglieder gespeichert sind, an die die Nachricht weitergeleitet wird, wenn das erste Teammitglied damit fertig ist.
  
|**Property Set**|**Second Team  <br/> Member**|**Drittes  <br/> Teammitglied**|**Viertes  <br/> Teammitglied**|
|:-----|:-----|:-----|:-----|
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Adresse = 0  <br/> |Adresse = 1  <br/> |Adresse = 2  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Adresstyp = 0  <br/> |Adresstyp = 1  <br/> |Adresstyp = 2  <br/> |
|PS_ROUTING_DISPLAY_NAME  <br/> |Anzeigename = 0  <br/> |Anzeigename = 1  <br/> |Anzeigename = 2  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Eintragsbezeichner = 0  <br/> |Eintragsbezeichner = 1  <br/> |Eintragsbezeichner = 2  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Suchschlüssel = 0  <br/> |Suchschlüssel = 1  <br/> |Suchschlüssel = 2  <br/> |
   
Clients, die zugeordnete Suchschlüssel als Verweise auf andere Nachrichteneigenschaften verwenden, müssen erkennen, dass die anderen Nachrichteneigenschaften erst übersetzt werden, wenn sie in einem dieser zugeordneten Eigenschaftensätze platziert werden. Wenn eine Nachricht mit nicht zugeordneten Verweisen auf zugeordnete Suchschlüssel an ein Ziel in einer anderen Messagingdomäne gesendet wird, sind die Verweise ungültig. Damit diese anderen Eigenschaften mit den Suchschlüsseln synchronisiert bleiben, können Sie ihnen Zeichenfolgennamen im PS_ROUTING_SEARCH_KEY Eigenschaftensatz zuweisen, die keine Konflikte mit den Namen aufweisen, die einer der wichtigsten zuordbaren Eigenschaften zugewiesen werden. Angenommen, ein Client muss eine Eigenschaft übertragen, die den Suchschlüssel für die letzte Person in einer langen Routingliste enthält. Der Client kann eine benannte Eigenschaft im PS_ROUTING_SEARCH_KEY Eigenschaftensatz namens "last_search_key" erstellen. Da sie in einem zugeordneten Eigenschaftensatz gespeichert ist, wird die Eigenschaft "last_search_key" zusammen mit den restlichen gatewayzuordnungsfähigen Eigenschaften übersetzt.
  

