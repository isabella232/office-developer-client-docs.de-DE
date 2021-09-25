---
title: Anzeigen von Konfigurationseigenschaftenblättern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 09283aa35b0f464822edc6b389f91a45ce135193
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551688"
---
# <a name="displaying-configuration-property-sheets"></a>Anzeigen von Konfigurationseigenschaftenblättern

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Transportanbieter verwenden die [IMAPISupport::D oConfigPropsheet-Methode,](imapisupport-doconfigpropsheet.md) um Konfigurationseigenschaftenblätter zu implementieren. Beim Aufrufen von **DoConfigPropSheet** übergibt der Transportanbieter einen Zeiger an ein Array von Eigenschaften zusammen mit Informationen zum Anzeigen dieser Eigenschaften. MapI stellt dem Benutzer dann die Eigenschaften mithilfe eines Standarddialogfelds vor. Es wird dringend empfohlen, diesen Eigenschaftenblattmechanismus zu verwenden, wenn Sie Ihren Transportanbieter implementieren, da der Benutzer von einer konsistenten Benutzeroberfläche profitieren kann.
  
## <a name="transport-providers"></a>Transportanbieter

Transportanbieter können die [BuildDisplayTable-Funktion](builddisplaytable.md) verwenden, um das Erstellen einer Anzeigetabelle für die Verwendung mit **DoConfigPropSheet** zu vereinfachen. Transportanbieter können die Eigenschaftenblatt-API auch direkt verwenden. Um Änderungen an den Eigenschaften zu puffern, können Transportanbieter die [CreateIProp-Funktion](createiprop.md) verwenden. Dies vereinfacht die Behandlung von Absagen durch den Benutzer, während der Benutzer die in den Eigenschaften gespeicherten Werte ändert. Bei Bedarf kann ein Transportanbieter auch ein Dialogfeld für den Assistenten bereitstellen, um Konfigurationsaufgaben für den Benutzer zu vereinfachen. 
  

