---
title: Verantwortlichkeiten für die Clientbenennung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dbb6ba5f-18c8-426f-9f50-ce6f2fd1dc5b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 808c7abf3d29872a8c5095fdc6dc39b2107a8993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424952"
---
# <a name="client-naming-responsibilities"></a>Verantwortlichkeiten für die Clientbenennung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients müssen eine Benennungskonvention für ihre Eigenschaften befolgen, die von einem Gateway übersetzt werden müssen. Alle zu übersetzenden Eigenschaften sollten als benannte Eigenschaften in einem der fünf Eigenschaftssätze erstellt werden, die für mappierbare Eigenschaften bestimmt sind:
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_ROUTING_SEARCH_KEY
  
Adressierungseigenschaften, die sich auf denselben Benutzer beziehen, müssen denselben Namen erhalten. Gateways verwenden diese Benennungskonvention, mit der sie eine Adresse mit dem richtigen Adresstyp übereinstimmen können. Bei der Adressparsierung muss die Zuordnung zwischen Adresse und Adresstyp genau sein.
  
MAPI-benannte Eigenschaften werden mit der **MAPINAMEID-Datenstruktur** dargestellt, die angibt, dass der Eigenschaftenname entweder eine Unicode-Zeichenfolge oder eine ganzzahlige 32-Bit-Zahl sein kann. Weitere Informationen finden Sie unter [MAPINAMEID](mapinameid.md). Die ganzzahlige Benennung wird für Adressgruppen empfohlen, da sie eine einfache Möglichkeit zum Unterscheiden zwischen Sätzen von behappbaren Eigenschaften darstellt und dem Benutzer problemlos als Index dienen kann. Die Alternative zur Verwendung ganzzahliger Zahlen besteht in der Zuweisung einer Zeichenfolge als Name für alle fünf mappablen Eigenschaften eines Benutzers. Wenn nur ein Benutzer eine Zuordnung erfordert, ist das Zuweisen einer Zeichenfolge akzeptabel. Wenn es jedoch mehrere Benutzer gibt, ist es besser, die ganzzahlige Benennung zu verwenden. Der Name, ob numerisch oder zeichenfolgenbasierter Name, sollte entweder in einer nachrichtenklassenspezifischen Eigenschaft oder in einer Eigenschaft gespeichert werden, die zu einem Eigenschaftensatz gehört, der von der Clientanwendung definiert wird. 
  
> [!NOTE]
> Vermeiden Sie die Übersetzung ganzzahliger Namen in Zeichenfolgen, z. B. "route_recipient_1" und "route_recipient_2". Dieser Aufwand ist unnötig. 
  
Um zu veranschaulichen, wie diese Benennungskonvention funktioniert, sollten Sie eine Routinganwendung in Betracht ziehen, die eine Nachricht an jedes Mitglied eines Vier-Personen-Teams sendet. Wenn ein Mitglied die Nachricht empfängt, muss es darauf antworten, bevor es zusammen mit den kompilierten Antworten an das nächste Mitglied gesendet werden kann. Die ursprüngliche Nachricht enthält eine Empfängerliste mit einem Eintrag: dem ersten Mitglied des Teams. Eingebettet in die Nachricht sind die Gateway-mappable-Eigenschaften für die anderen drei Teammitglieder. Jedes Mitglied verfügt über fünf Kernbenutzereigenschaften, die sich in den Gateway-mappable-Eigenschaftssätzen befinden, denen eine eindeutige Zahl als Name zugewiesen ist. 
  
In der folgenden Tabelle sind die Einstellungen für jeden Satz von Gatewayeigenschaften dargestellt, die für die drei verbleibenden Teammitglieder gespeichert sind, an die die Nachricht geroutet wird, wenn das erste Teammitglied damit fertig ist.
  
|**Property Set**|**Zweites  <br/> Teammitglied**|**Drittes  <br/> Teammitglied**|**Viertes  <br/> Teammitglied**|
|:-----|:-----|:-----|:-----|
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Adresse = 0  <br/> |Adresse = 1  <br/> |Adresse = 2  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Adresstyp = 0  <br/> |Adresstyp = 1  <br/> |Adresstyp = 2  <br/> |
|PS_ROUTING_DISPLAY_NAME  <br/> |Anzeigename = 0  <br/> |Anzeigename = 1  <br/> |Anzeigename = 2  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Eintrags-ID = 0  <br/> |Eintrags-ID = 1  <br/> |Eintrags-ID = 2  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Suchtaste = 0  <br/> |Suchtaste = 1  <br/> |Suchtaste = 2  <br/> |
   
Clients, die anpassbare Suchschlüssel als Verweise auf andere Nachrichteneigenschaften verwenden, müssen erkennen, dass die anderen Nachrichteneigenschaften nur übersetzt werden, wenn sie in einem dieser mappable-Eigenschaftssätze platziert werden. Wenn eine Nachricht mit nicht zugeordneten Verweisen auf zugeordnete Suchschlüssel an ein Ziel in einer anderen Messagingdomäne gesendet wird, sind die Verweise ungültig. Damit diese anderen Eigenschaften mit den Suchschlüsseln synchronisiert bleiben, können Sie ihnen Zeichenfolgennamen im PS_ROUTING_SEARCH_KEY-Eigenschaftensatz zuweisen, die keine Auswirkungen auf die Namen haben, die für die wichtigsten mappbaren Eigenschaften angegeben werden. Angenommen, ein Client muss eine Eigenschaft übertragen, die den Suchschlüssel für die letzte Person in einer langen Routingliste enthält. Der Client kann eine benannte Eigenschaft im eigenschaftensatz PS_ROUTING_SEARCH_KEY namens "last_search_key" erstellen. Da sie in einem mappable-Eigenschaftssatz gespeichert ist, wird die "last_search_key"-Eigenschaft zusammen mit den restlichen Gateway-mappable-Eigenschaften übersetzt.
  

