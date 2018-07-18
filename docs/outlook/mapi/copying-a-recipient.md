---
title: Kopieren eines Empfängers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dd68bc2054136a7f587b05dc56dbeabd06de1f08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791459"
---
# <a name="copying-a-recipient"></a>Kopieren eines Empfängers

  
  
**Betrifft**: Outlook 
  
Um einen oder mehrere Empfänger aus einem Container in ein anderes oder den gleichen Container kopieren, Sie zunächst sicher, dass der Zielcontainer geändert werden kann. Container, die geändert werden festlegen AB_MODIFIABLE Flag in ihre **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))-Eigenschaft.
  
Um einen oder mehrere Einträge in einem änderbare Container zu kopieren, rufen Sie das Ziel des Containers [IABContainer::CopyEntries](iabcontainer-copyentries.md) -Methode. Da Kopieren von Adressbucheinträgen zeitaufwendig sein kann, **CopyEntries** akzeptiert vier Eingabeparameter: ein Array von Eintragsbezeichner für die Einträge kopiert werden soll, ein Fensterhandle, eine Statusanzeige und eine Bitmaske aus Flags. 
  
Das Fenster Handle und Fortschritt Symbol werden von der Adressbuchanbieter verwendet, um den Status des Vorgangs für dem Benutzer anzuzeigen. Wenn Sie Status anzeigen möchten, übergeben Sie ein Fensterhandle für das übergeordnete Fenster der Statusanzeige in der _UlUIParam_ -Parameter, und legen Sie das Flag AB_NO_DIALOG nicht im Parameter _UlFlags_ . Wenn Sie eine eigene Implementierung einer Statusanzeige haben, übergeben Sie einen Zeiger an die Implementierung der im Parameter _LpProgress_ . Wenn dies nicht der Fall ist, übergeben Sie NULL. Der Adressbuchanbieter wird die MAPI-Fortschritt Indikator Implementierung verwenden. 
  
Die Bitmaske der Kennzeichen gibt an, unabhängig davon, ob eine Statusanzeige angezeigt werden soll und wie doppelter Eintrag Überprüfung behandelt werden sollen. Legen Sie die Kennzeichen AB_NO_DIALOG unterdrückt werden, eine Statusanzeige. Legen Sie das Kennzeichen CREATE_CHECK_DUP_LOOSE angewiesen, die Adressbuchanbieter lose Suche nach Duplikaten oder das CREATE_CHECK_DUP_STRICT-Flag für strengere doppelte überprüfen. Set das CREATE_REPLACE-Flag Einträge kopiert haben Ersetzen der vorhandenen Einträge aus, wenn der Anbieter wird bestimmt, ob Duplikate vorhanden sind. 
  
Beim Kopieren in einer persönlichen Adressbuchcontainer (PAB) werden der Anbieter einige oder alle Eigenschaften für jeden Eintrag kopiert. Da MAPI-Anforderungen für Anbieter implementieren von Vorgängen zum Container nicht hergestellt wird, nicht möglich Sie Annahmen über die Anzahl und Typ der Eigenschaften, die mit einem Address Book Eintrag kopiert werden.
  

