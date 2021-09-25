---
title: Kopieren eines Empfängers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c9030d9341ba9aea0ce186ba4205242e5e65b1fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617048"
---
# <a name="copying-a-recipient"></a>Kopieren eines Empfängers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um einen oder mehrere Empfänger aus einem Container in einen anderen oder denselben Container zu kopieren, überprüfen Sie zunächst, ob der Zielcontainer modifizierbar ist. Container, die modifizierbar sind, legen die AB_MODIFIABLE-Kennzeichnung in ihrer **PR_CONTAINER_FLAGS** -[PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) -Eigenschaft fest.
  
Um einen oder mehrere Einträge in einen modifizierbaren Container zu kopieren, rufen Sie die [IABContainer::CopyEntries-Methode](iabcontainer-copyentries.md) des Zielcontainers auf. Da das Kopieren von Adressbucheinträgen zeitaufwändig sein kann, akzeptiert **CopyEntries** vier Eingabeparameter: ein Array von Eintragsbezeichnern für die zu kopierenden Einträge, ein Fensterhandle, eine Statusanzeige und eine Bitmaske mit Flags. 
  
Das Fensterhandle und die Statusanzeige werden vom Adressbuchanbieter verwendet, um dem Benutzer den Status des Vorgangs anzuzeigen. Wenn Sie den Fortschritt anzeigen möchten, übergeben Sie ein Fensterhandle für das übergeordnete Fenster der Statusanzeige im  _ulUIParam-Parameter,_ und legen Sie das flag AB_NO_DIALOG im  _ulFlags-Parameter_ nicht fest. Wenn Sie eine eigene Implementierung einer Statusanzeige haben, übergeben Sie einen Zeiger an die Implementierung im _lpProgress-Parameter._ Wenn nicht, übergeben Sie NULL. Der Adressbuchanbieter verwendet die Implementierung der MAPI-Statusanzeige. 
  
Die Bitmaske von Flags gibt an, ob Sie eine Statusanzeige anzeigen möchten und wie die Überprüfung doppelter Einträge behandelt werden soll. Legen Sie das AB_NO_DIALOG-Kennzeichen fest, um eine Statusanzeige zu unterdrücken. Legen Sie das flag CREATE_CHECK_DUP_LOOSE fest, um den Adressbuchanbieter anzuweisen, lose nach Duplikaten zu suchen, oder das Flag CREATE_CHECK_DUP_STRICT für eine strengere Duplikatprüfung. Legen Sie das CREATE_REPLACE Flag fest, damit kopierte Einträge vorhandene Einträge ersetzen, wenn der Anbieter feststellt, dass Duplikate vorhanden sind. 
  
Beim Kopieren in einen PAB-Container (Personal Address Book) kopiert der Anbieter einige oder alle Eigenschaften für jeden Eintrag. Da die MAPI keine Anforderungen für Anbieter festlegt, die Containerkopievorgänge implementieren, können Sie keine Annahmen über die Anzahl und den Typ der Eigenschaften treffen, die mit einem Adressbucheintrag kopiert werden.
  

