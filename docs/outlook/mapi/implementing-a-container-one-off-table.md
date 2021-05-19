---
title: Implementieren einer One-Off-Tabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417420"
---
# <a name="implementing-a-container-one-off-table"></a>Implementieren einer One-Off-Tabelle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um auf die einmal zu einem Ihrer Container gehörende Tabelle zu zugreifen, ruft MAPI die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Containers auf, um die **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md))-Eigenschaft mit der **IMAPITable-Schnittstelle** zu öffnen. Ihr Container wird aufgefordert, seine einmal aufgeführte Tabelle zurückzukehren, wenn eine Clientanwendung versucht, dem Container einen Empfänger hinzuzufügen. Wenn der Container Empfänger zulässt, kann Ihr Anbieter entweder eine eigene Tabellenimplementierung zurückgeben oder [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) aufrufen, um die MAPI-Implementierung zurückzukehren. 
  
Der Satz von Vorlagen in der Einmaltabelle des Containers sollte den Empfängertyp widerspiegeln, den der bestimmte Container enthalten kann. In der Regel umfasst dies eine oder zwei Vorlagen, Vorlagen zum Erstellen eines einzelnen Messagingbenutzers oder einer Verteilerliste. Die Eintragsbezeichner für diese Vorlagen werden in den **Eigenschaften PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) und **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) enthalten. Container sind jedoch keinesfalls auf diese Arten von Einträgen beschränkt. Sie können andere Arten von Empfängern oder Nicht-Empfänger-Einträgen wie Verzeichnisse enthalten. 
  

