---
title: Implementieren einer Container-Einmaltabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d468943f84f1d23f1b4b84881e69cee0041a5bae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576596"
---
# <a name="implementing-a-container-one-off-table"></a>Implementieren einer Container-Einmaltabelle

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Zugriff auf die einmalige Tabelle einer von Ihrer Containern MAPI des Containers [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode zum Öffnen der **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md))-Eigenschaft mit der **IMAPITable** aufgerufen Schnittstelle. Der Container wird gefragt, seine einmalige Tabelle zurückzugeben, wenn eine Clientanwendung versucht, einen Empfänger an den Container hinzuzufügen. Wenn der Container Empfänger zulässt, kann vom Dienstanbieter entweder eine eigene Tabelle-Implementierung zurückzugeben oder [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) , um die MAPI-Implementierung zurückzugeben. 
  
Die Gruppe der Vorlagen in der einmaligen Container-Tabelle sollte den Typ der Empfänger wieder, die der jeweiligen Container enthalten kann. Dies umfasst in der Regel ein oder zwei Vorlagen, Vorlagen für die Erstellung einer einzelnen messaging-Benutzer oder eine Verteilerliste. Für diese Vorlagen den Eintrag-IDs werden in die **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) und **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) Eigenschaften gehalten. Container sind jedoch nicht auf diese Arten von Einträgen beschränkt. Sie können andere Typen von Empfängern oder nicht-Recipient Einträge wie Verzeichnisse enthalten. 
  

