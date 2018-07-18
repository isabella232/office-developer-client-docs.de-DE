---
title: MAPI-Adressbuch
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6703ba3f-54a5-4059-b10a-1d42a9e81be1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b328a65f400e424fb2cd177e710fb8bcffa392c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792928"
---
# <a name="mapi-address-book"></a>MAPI-Adressbuch

  
  
**Betrifft**: Outlook 
  
Integrierte des Adressbuchs ist ein Objekt, MAPI, um Zugriff auf eine integrierte Sammlung von Adressinformationen aus allen im Profil der adressbuchanbietern implementierte implementiert. Mit dem Adressbuch-Clientanwendungen und Dienstanbieter keine zur Unterscheidung zwischen den eindeutigen Adressierungsschemas von messaging-Systeme. Stattdessen k�nnen sie die Adressen der Empf�nger in messaging-System, nachschlagen, solange der Adressbuchanbieter f�r die messaging-System installiert ist.
  
Das Adressbuch kann ohne Benutzereingriff oder interaktiv durch Verwendung der Standarddialogfelder programmgesteuert zugegriffen werden. MAPI enth�lt Dialogfelder zum Anzeigen einer Zusammenfassungsliste der Eintr�ge im Adressbuch, detaillierte Informationen zu einem bestimmten Empf�nger, eine Warnung ausgegeben, wenn ein Benutzer einen Empf�nger erstellt, der eine eindeutige Adresse und eine Reihe von vorlagenformulare zum Erstellen von neuen Empf�nger zugeordnet werden kann.
  
Das MAPI-Adressbuch �hnelt in der Struktur einen Nachrichtenspeicher, dass es hierarchisch organisiert werden. Das Adressbuch bietet Zugriff auf drei Arten von Objekten, die durch ein Adressbuchanbieter implementiert:
  
- Ein Address Book Container-Objekt.
    
- Verteilung von List-Objekt.
    
- Ein messaging User-Objekt.
    
Jeder dieser Typen von Objekten erfolgt �ber dessen eindeutige Eintrags-ID, die von der Adressbuchanbieter zugewiesen ist. 
  
Address Book Containern �hneln Ordner darin, dass sie Objekte mit unterschiedlichen Typen enthalten. Ein Adressbuchcontainer kann andere Address Book Container sowie Benutzer- und Verteilung Listenobjekten messaging halten. Address Book Containern dienen zum Organisieren und Speichern von Address Book-Objekten.
  
Um das Adressbuch integrierte Darstellung zu erreichen, verf�gbar machen von adressbuchanbietern implementierte, keinen, einen oder mehrere der ihre Container MAPI werden und zeigt die Ergebnisse unter einer einzigen Container der obersten Ebene auf oberster Ebene. Von adressbuchanbietern implementierte k�nnen ausw�hlen, um eine Gruppe von Containern f�r einen Typ von messaging-Sitzung und eine andere Gruppe f�r eine andere Sitzung verf�gbar zu machen. Es ist au�erdem m�glich, dass von adressbuchanbietern implementierte haben keine Container auf oberster Ebene und verf�gbar zu machen nur eine Liste der Vorlagen, die zum Erstellen von Empf�ngern verwendet werden k�nnen.
  
Empf�nger der Nachricht werden mit der messaging-Benutzer und Verteilung Listenobjekten implementiert. Messaging-Benutzer sind einzelne Empf�nger. Verteilerlisten, Empf�nger Gruppe sind. Jeder messaging Benutzer verf�gt �ber eine eindeutige Adresse eines bestimmten Typs von einem bestimmten messaging-System behandelt. Eine Verteilerliste ist eine benannte Auflistung von Empf�ngern. Verteilerlisten k�nnen messaging User-Objekte und andere Verteilerlisten enthalten. Wenn ein Benutzer von einer Clientanwendung an eine Verteilerliste eine Nachricht sendet, wird die Nachricht an alle Mitglieder der Liste messaging Benutzer gesendet wird. 
  
Messaging-Benutzer und Verteilerlisten weist eine Reihe von f�nf Eigenschaften, die als die Eigenschaften Basisadresse bezeichnet werden. Erforderliche Eigenschaften werden und sind wie folgt kurz beschrieben.
  
|**Basisadresse-Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Adresstyp f�r den Empf�nger. Jeden Adresstyp folgt ein bestimmtes Format und mit einem bestimmten messaging-System verwendet wird.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Anzeigename f�r den Empf�nger.  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Die Adresse des Empf�ngers.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Eintrags-ID verwendet, um den Empf�nger zuzugreifen.  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Bin�re vergleichbaren Schl�ssel verwendet, um den Empf�nger zu identifizieren.  <br/> |
   
MAPI definiert viele Gruppen von Eigenschaften, die Variationen der Basisadresse Eigenschaften sind. Diese anderen Gruppen werden messaging-Benutzer und Verteilerlisten in verschiedenen Situationen beschrieben. Beispielsweise wird eine Gruppe von Eigenschaften den Delegaten Absender eine Nachricht und eine andere Gruppe der Stellvertretung Empf�nger beschrieben.
  

