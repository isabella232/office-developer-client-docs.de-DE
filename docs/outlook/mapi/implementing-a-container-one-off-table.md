---
title: Implementieren einer Container-One-Off-Tabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 62951a7c4330fb8e909e0b6b978c210a5f5c1938
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610496"
---
# <a name="implementing-a-container-one-off-table"></a>Implementieren einer Container-One-Off-Tabelle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um auf die einmalige Tabelle zuzugreifen, die zu einem Ihrer Container gehört, ruft MAPI die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Containers auf, um die **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) -Eigenschaft mit der **IMAPITable-Schnittstelle** zu öffnen. Ihr Container wird aufgefordert, seine einmalige Tabelle zurückzugeben, wenn eine Clientanwendung versucht, dem Container einen Empfänger hinzuzufügen. Wenn der Container Empfänger zulässt, kann Ihr Anbieter entweder eine eigene Tabellenimplementierungen zurückgeben oder [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) aufrufen, um die MAPI-Implementierung zurückzugeben. 
  
Der Vorlagensatz in der einmaligen Containertabelle sollte den Empfängertyp widerspiegeln, den der jeweilige Container enthalten kann. In der Regel umfasst dies eine oder zwei Vorlagen, Vorlagen zum Erstellen eines einzelnen Messagingbenutzers oder einer Verteilerliste. Die Eintragsbezeichner für diese Vorlagen befinden sich in den Eigenschaften **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) und **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). Container sind jedoch keinesfalls auf diese Arten von Einträgen beschränkt. Sie können andere Arten von Empfängern oder Einträge enthalten, die keine Empfänger sind, z. B. Verzeichnisse. 
  

