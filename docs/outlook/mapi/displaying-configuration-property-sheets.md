---
title: Anzeigen von Konfigurationseigenschaftenblättern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a796f458e9d30206dc4c6feb37cbdb1e6b6a704b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421312"
---
# <a name="displaying-configuration-property-sheets"></a>Anzeigen von Konfigurationseigenschaftenblättern

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Transport Anbieter verwenden die [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) -Methode, um Konfigurationseigenschaften Blätter zu implementieren. Beim Aufrufen von **DoConfigPropSheet**übergibt der Transportanbieter einen Zeiger auf ein Array von Eigenschaften sowie Informationen dazu, wie diese angezeigt werden. Anschließend werden die Eigenschaften dem Benutzer mithilfe eines Standarddialogfelds angezeigt. Es wird dringend empfohlen, diesen Eigenschaftenblatt Mechanismus bei der Implementierung Ihres Transportanbieters zu verwenden, da der Benutzer eine konsistente Schnittstelle nutzen können.
  
## <a name="transport-providers"></a>Transport Anbieter

Transport Anbieter können die [BuildDisplayTable](builddisplaytable.md) -Funktion verwenden, um die Erstellung einer Anzeigetabelle für die Verwendung mit **DoConfigPropSheet**zu vereinfachen. Transport Anbieter können auch die Eigenschaftenblatt-API direkt verwenden. Zum Puffern von Änderungen an den Eigenschaften können Transportanbieter die [CreateIProp](createiprop.md) -Funktion verwenden. Dies vereinfacht die Behandlung von absagen durch den Benutzer, während der Benutzer die in den Eigenschaften gespeicherten Werte ändert. Falls erforderlich, kann ein Transportanbieter auch ein Dialogfeld des Assistenten bereitstellen, um Konfigurationsaufgaben für den Benutzer zu vereinfachen. 
  

