---
title: Kopieren eines Empfängers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3a4fb1a3f76481bf1960c251a33911b871a8791c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419086"
---
# <a name="copying-a-recipient"></a>Kopieren eines Empfängers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um einen oder mehrere Empfänger aus einem Container in einen anderen oder denselben Container zu kopieren, überprüfen Sie zunächst, ob der Zielcontainer veränderbar ist. Container, die veränderbar sind, legen AB_MODIFIABLE -Flag in ihrer **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) -Eigenschaft fest.
  
Um einen oder mehrere Einträge in einen veränderbaren Container zu kopieren, rufen Sie die [IABContainer::CopyEntries-Methode des Zielcontainers](iabcontainer-copyentries.md) auf. Da das Kopieren von Adressbucheinträgen zeitaufwändig sein kann, akzeptiert **CopyEntries** vier Eingabeparameter: ein Array von Eingabebezeichnern für die zu kopierenden Einträge, ein Fensterhandle, eine Statusanzeige und eine Bitmaske mit Flags. 
  
Das Fensterhandle und die Statusanzeige werden vom Adressbuchanbieter verwendet, um dem Benutzer den Status des Vorgangs anzuzeigen. Wenn Sie den Fortschritt anzeigen möchten, übergeben Sie ein Fensterhandle für das übergeordnete Fenster der Statusanzeige im _ulUIParam-Parameter,_ und legen Sie nicht das AB_NO_DIALOG im _ulFlags-Parameter._ Wenn Sie über eine eigene Implementierung eines Fortschrittsindikators verfügen, übergeben Sie einen Zeiger auf die Implementierung im _lpProgress-Parameter._ Wenn nicht, übergeben Sie NULL. Der Adressbuchanbieter verwendet die Implementierung des MAPI-Fortschrittsindikators. 
  
Die Bitmaske der Flags gibt an, ob sie eine Statusanzeige anzeigen möchten und wie die Überprüfung doppelter Einträge behandelt werden soll. Legen Sie das AB_NO_DIALOG, um eine Statusanzeige zu unterdrücken. Legen Sie CREATE_CHECK_DUP_LOOSE,um den Adressbuchanbieter anweisen, auf Duplikate oder das CREATE_CHECK_DUP_STRICT auf eine strengere Duplikatprüfung zu überprüfen. Legen Sie CREATE_REPLACE, dass kopierte Einträge vorhandene Einträge ersetzen, wenn der Anbieter feststellt, dass Duplikate vorhanden sind. 
  
Beim Kopieren in einen persönlichen Adressbuchcontainer kopiert der Anbieter einige oder alle Eigenschaften für jeden Eintrag. Da MAPI keine Anforderungen für Anbieter mit Containerkopievorgängen stellt, können Sie keine Annahmen über die Anzahl und den Typ der Eigenschaften machen, die mit einem Adressbucheintrag kopiert werden.
  

