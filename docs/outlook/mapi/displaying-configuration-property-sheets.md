---
title: Anzeigen der Konfiguration Eigenschaftenseiten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: aa3ddecbd5af56eef16f5ae3a349a027e689fc8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791562"
---
# <a name="displaying-configuration-property-sheets"></a>Anzeigen der Konfiguration Eigenschaftenseiten

**Betrifft**: Outlook 
  
Transportanbieter für verwenden Sie die Methode [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) Konfiguration Eigenschaftenseiten zu implementieren. Beim Aufruf von **DoConfigPropSheet**übergibt der Adressbuchhierarchie einen Zeiger auf ein Array von Eigenschaften sowie Informationen dazu, wie sie angezeigt. MAPI stellt dann die Eigenschaften für den Benutzer über ein standard-Dialogfeld. Es wird dringend empfohlen, diese Eigenschaft Blatt-Mechanismus verwenden, wenn Ihre Adressbuchhierarchie aufgrund der Vorteil für den Benutzer über eine konsistente Schnittstelle implementieren.
  
## <a name="transport-providers"></a>Transportanbieter

Transportanbieter können die [BuildDisplayTable](builddisplaytable.md) -Funktion verwenden, um das Erstellen einer Tabelle anzeigen, für die Verwendung mit **DoConfigPropSheet**vereinfachen. Transportanbieter können auch direkt auf die Eigenschaftenblatt-API zu. Änderungen an den Eigenschaften Puffer, transport-Anbieter können die [CreateIProp](createiprop.md) -Funktion verwenden. Dies vereinfacht die Behandlung von Absagen vom Benutzer während der Benutzer die Werte in den Eigenschaften gespeichert geändert. Wenn erforderlich, ein Transportdienstes auch ein Dialogfeld Assistent für bereitstellen kann im Feld, um die Konfigurationsaufgaben für den Benutzer zu vereinfachen. 
  

