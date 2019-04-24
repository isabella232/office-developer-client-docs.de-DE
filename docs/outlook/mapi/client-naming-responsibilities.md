---
title: Verantwortlichkeiten für die beNennung von Clients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dbb6ba5f-18c8-426f-9f50-ce6f2fd1dc5b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 808c7abf3d29872a8c5095fdc6dc39b2107a8993
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335140"
---
# <a name="client-naming-responsibilities"></a>Verantwortlichkeiten für die beNennung von Clients

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients müssen eine Benennungskonvention für ihre Eigenschaften befolgen, die von einem Gateway übersetzt werden müssen. Alle zu übersetzenden Eigenschaften sollten als benannte Eigenschaften in einem der fünf Eigenschaftssätze erstellt werden, die zuzuordnende-Eigenschaften enthalten:
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_ROUTING_SEARCH_KEY
  
Die Adressierung von Eigenschaften, die sich auf denselben Benutzer beziehen, muss denselben Namen haben. Gateways basieren auf dieser Benennungskonvention, die es Ihnen ermöglicht, eine Adresse mit dem richtigen Adresstyp zu vergleichen. Für die Adressanalyse muss die Zuordnung zwischen Adresse und Adresstyp genau sein.
  
MAPI-benannte Eigenschaften werden mit der **MAPINAMEID** -Datenstruktur dargestellt, die angibt, dass es sich bei dem Eigenschaftennamen um eine Unicode-Zeichenfolge oder eine 32-Bit-Ganzzahl handeln kann. Weitere Informationen finden Sie unter [MAPINAMEID](mapinameid.md). Ganz Zahl Benennungen werden für Gruppen von Adressen empfohlen, da es sich um eine einfache Möglichkeit zur Unterscheidung zwischen zuzuordnende-Eigenschaften handelt, und Sie können dem Benutzer problemlos als Index dienen. Die Alternative zur Verwendung von ganzen Zahlen ist das Zuweisen einer Zeichenfolge als Namen für alle fünf zuzuordnende-Eigenschaften eines Benutzers. Wenn nur ein Benutzer eine Zuordnung erfordert, ist das Zuweisen einer Zeichenfolge zulässig. Wenn es jedoch mehrere Benutzer gibt, empfiehlt es sich, die ganz Zahl Benennung zu verwenden. Der Name, unabhängig davon, ob er numerisch oder Zeichenfolgen basiert ist, sollte entweder in einer Nachrichtenklassen spezifischen Eigenschaft oder in einer Eigenschaft gespeichert werden, die zu einem Eigenschaftensatz gehört, der von der Clientanwendung definiert wird. 
  
> [!NOTE]
> Vermeiden Sie die Übersetzung von ganzzahligen Namen in Zeichenfolgen wie "route_recipient_1" und "route_recipient_2". Dieser Aufwand ist nicht erforderlich. 
  
Um zu veranschaulichen, wie diese Benennungskonvention funktioniert, sollten Sie eine Routing Anwendung erwägen, die eine Nachricht an jedes Mitglied eines vierköpfigen Teams sendet. Wenn ein Mitglied die Nachricht erhält, muss Sie darauf antworten, bevor es zusammen mit den kompilierten Antworten an das nächste Mitglied gesendet werden kann. Die ursprüngliche Nachricht enthält eine Empfängerliste mit einem Eintrag: das erste Mitglied des Teams. Eingebettet in die Nachricht sind die Gateway-zuzuordnende-Eigenschaften für die anderen drei Teammitglieder. Jedes Mitglied verfügt über fünf Hauptbenutzer Eigenschaften, die sich in den zuzuordnende-Eigenschaftssätzen befinden, denen eine eindeutige Nummer als Name zugewiesen wird. 
  
In der folgenden Tabelle sind die Einstellungen für jede Gruppe von Gateway-zuzuordnende-Eigenschaften dargestellt, die für die drei verbleibenden Teammitglieder gespeichert sind, an die die Nachricht weitergeleitet wird, wenn das erste Teammitglied damit fertig ist.
  
|**Property Set**|**Zweites Team <br/> Mitglied**|**Drittes <br/> Team Mitglied**|**Viertes <br/> Team Mitglied**|
|:-----|:-----|:-----|:-----|
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Adresse = 0  <br/> |Adresse = 1  <br/> |Adresse = 2  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Adresstyp = 0  <br/> |Adresstyp = 1  <br/> |Adresstyp = 2  <br/> |
|PS_ROUTING_DISPLAY_NAME  <br/> |Anzeigename = 0  <br/> |Anzeigename = 1  <br/> |Anzeigename = 2  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Eintrags-ID = 0  <br/> |Eintrags-ID = 1  <br/> |Eintrags-ID = 2  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Suchschlüssel = 0  <br/> |Suchschlüssel = 1  <br/> |Suchschlüssel = 2  <br/> |
   
Clients, die zuzuordnende-Suchschlüssel als Verweise auf andere Nachrichteneigenschaften verwenden, müssen erkennen, dass die anderen Nachrichteneigenschaften nur dann übersetzt werden, wenn Sie in einem dieser zuzuordnende-Eigenschaftensätze enthalten sind. Wenn eine Nachricht mit nicht zugeordneten verweisen auf zugeordnete Suchschlüssel an ein Ziel in einer anderen Messaging Domäne gesendet wird, sind die Verweise ungültig. Um zu ermöglichen, dass diese anderen Eigenschaften mit den Such Schlüsseln synchronisiert bleiben, können Sie diese Zeichenfolgennamen im PS_ROUTING_SEARCH_KEY-Eigenschaftensatz zuweisen, die nicht die Namen der wichtigsten zuzuordnende-Eigenschaften beeinträchtigen. Angenommen, ein Client muss eine Eigenschaft übermitteln, die den Suchschlüssel für die letzte Person in einer langen Routingliste enthält. Der Client kann eine benannte Eigenschaft im PS_ROUTING_SEARCH_KEY-Eigenschaftensatz mit dem Namen "last_search_key" erstellen. Da es in einem zuzuordnende-Eigenschaftensatz gespeichert ist, wird die "last_search_key"-Eigenschaft zusammen mit den restlichen Gateway-zuzuordnende-Eigenschaften übersetzt.
  

