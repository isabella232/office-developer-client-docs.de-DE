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
  
Transportanbieter verwenden die [IMAPISupport::D oConfigPropsheet-Methode,](imapisupport-doconfigpropsheet.md) um Konfigurationseigenschaftenblätter zu implementieren. Beim Aufrufen **von DoConfigPropSheet** übergibt der Transportanbieter einen Zeiger an ein Array von Eigenschaften sowie Informationen zum Anzeigen dieser Eigenschaften. MAPI stellt die Eigenschaften dann dem Benutzer über ein Standarddialogfeld vor. Sie werden dringend aufgefordert, diesen Eigenschaftenblattmechanismus bei der Implementierung Ihres Transportanbieters zu verwenden, da der Benutzer von einer konsistenten Schnittstelle profitieren kann.
  
## <a name="transport-providers"></a>Transportanbieter

Transportanbieter können die [BuildDisplayTable-Funktion](builddisplaytable.md) verwenden, um die Erstellung einer Anzeigetabelle für die Verwendung mit **DoConfigPropSheet zu vereinfachen.** Transportanbieter können auch die Eigenschaftenblatt-API direkt verwenden. Zum Puffern von Änderungen an den Eigenschaften können Transportanbieter die [CreateIProp-Funktion](createiprop.md) verwenden. Dies vereinfacht die Behandlung von Stornierungen durch den Benutzer, während der Benutzer die in den Eigenschaften gespeicherten Werte ändert. Bei Bedarf kann ein Transportanbieter auch ein Dialogfeld zum Vereinfachen von Konfigurationsaufgaben für den Benutzer bereitstellen. 
  

