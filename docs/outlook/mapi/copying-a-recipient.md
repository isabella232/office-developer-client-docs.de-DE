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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333061"
---
# <a name="copying-a-recipient"></a>Kopieren eines Empfängers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie einen oder mehrere Empfänger aus einem Container in einen anderen oder denselben Container kopieren möchten, überprüfen Sie zunächst, ob der Zielcontainer veränderbar ist. Zu ändernde Container legen Sie das AB_MODIFIABLE-Flag in Ihrer **PR_CONTAINER_FLAGS** ([pidtagcontainerflags (](pidtagcontainerflags-canonical-property.md))-Eigenschaft fest.
  
Wenn Sie einen oder mehrere Einträge in einen änderbaren Container kopieren möchten, rufen Sie die [IABContainer:: CopyEntries](iabcontainer-copyentries.md) -Methode des Zielcontainers auf. Da das Kopieren von Adressbucheinträgen zeitaufwändig sein kann, akzeptiert **CopyEntries** vier Eingabeparameter: ein Array von Eintrags Bezeichnern für die zu kopierenden Einträge, ein Fensterhandle, eine Statusanzeige und eine Bitmaske von Flags. 
  
Das Fensterhandle und die Statusanzeige werden vom Adressbuchanbieter verwendet, um dem Benutzer den Status des Vorgangs anzuzeigen. Wenn Sie den Fortschrittanzeigen möchten, übergeben Sie ein Fensterhandle für das übergeordnete Fenster der Statusanzeige im _ulUIParam_ -Parameter, und legen Sie das AB_NO_DIALOG-Flag im _ulFlags_ -Parameter nicht fest. Wenn Sie über eine Statusanzeige verfügen, übergeben Sie einen Zeiger an die Implementierung im _lpProgress_ -Parameter. Wenn dies nicht der Fall ist, führen Sie NULL aus. Der Adressbuchanbieter verwendet die MAPI-Statusindikator Implementierung. 
  
Die Bitmaske der Flags gibt an, ob eine Statusanzeige angezeigt werden soll und wie die Überprüfung der doppelten Eingabe erfolgen soll. Legen Sie das AB_NO_DIALOG-Flag fest, um eine Statusanzeige zu unterdrücken. Legen Sie das CREATE_CHECK_DUP_LOOSE-Flag fest, um den Adressbuchanbieter anzuweisen, auf Duplikate oder das CREATE_CHECK_DUP_STRICT-Flag für strengere Duplikatprüfung zu prüfen. Legen Sie das CREATE_REPLACE-Flag so fest, dass kopierte Einträge vorhandene Einträge ersetzen, wenn der Anbieter feststellt, dass Duplikate vorhanden sind. 
  
Beim Kopieren in einen PAB-Container (persönliches Adressbuch) kopiert der Anbieter einige oder alle Eigenschaften für jeden Eintrag. Da MAPI keine Anforderungen für Anbieter festlegt, die Container Kopiervorgänge implementieren, können Sie keine Annahmen über die Anzahl und den Typ von Eigenschaften treffen, die mit einem Adressbucheintrag kopiert werden.
  

