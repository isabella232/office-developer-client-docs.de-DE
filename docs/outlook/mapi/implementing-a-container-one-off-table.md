---
title: Implementieren einer Container-einmal Tabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332886"
---
# <a name="implementing-a-container-one-off-table"></a>Implementieren einer Container-einmal Tabelle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um auf die einmalige Tabelle zuzugreifen, die zu einem ihrer Container gehört, ruft MAPI die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Containers auf, um die **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md))-Eigenschaft mit der **IMAPITable** zu öffnen. Oberfläche. Der Container wird aufgefordert, seine einmalige Tabelle zurückzugeben, wenn eine Clientanwendung versucht, dem Container einen Empfänger hinzuzufügen. Wenn der Container Empfänger zulässt, kann Ihr Anbieter entweder eine eigene Tabellen Implementierung zurückgeben oder [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md) aufrufen, um die MAPI-Implementierung zurückzugeben. 
  
Der Vorlagensatz in der einmaligen Container Tabelle sollte den Typ der Empfänger widerspiegeln, die der jeweilige Container enthalten kann. Dies umfasst in der Regel eine oder zwei Vorlagen, Vorlagen zum Erstellen eines einzelnen Messaging Benutzers oder einer Verteilerliste. Die Eintragsbezeichner für diese Vorlagen werden in den Eigenschaften **PR_DEF_CREATE_MAILUSER** ([Pidtagdefcreatemailuser (](pidtagdefcreatemailuser-canonical-property.md)) und **PR_DEF_CREATE_DL** ([pidtagdefcreatedl (](pidtagdefcreatedl-canonical-property.md)) gespeichert. Container sind jedoch keineswegs auf diese Art von Einträgen beschränkt. Sie können andere Typen von Empfängern oder nicht Empfänger Einträgen wie Verzeichnissen enthalten. 
  

