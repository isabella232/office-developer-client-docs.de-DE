---
title: Ungültigen eines Objekts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf7ef15ccfd9cd015771785bda9d6ad79415736b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407676"
---
# <a name="invalidating-an-object"></a>Ungültigen eines Objekts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im Rahmen des Herunterfahrens Ihres Anbieters möchten Sie möglicherweise ein Objekt ungültig erklären. Das Ungültigen eines Objekts umfasst das Ersetzen der vtable durch eine vtable, die Implementierungen für die drei **IUnknown-Methoden** **enthält: AddRef**, **Release** und **QueryInterface**. Ungültig machen Sie ein Objekt, indem [Sie IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)aufrufen, eine Methode, die im Supportobjekt der drei gängigen Anbietertypen enthalten ist. Anbieter rufen diesen Aufruf in der Regel in der Implementierung der **Logoff-Methode** des Anmeldeobjekts ab. 
  
Durch die Ungültigkeit eines Objekts ist MAPI letztendlich für die Speicherfreispeicherung verantwortlich, die einem Objekt zugeordnet ist. Sie können alle ressourcen frei, die mit einem Objekt verbunden sind, und **makeInvalid** aufrufen, um alle Methoden in den geerbten Schnittstellen ungültig zu machen. Aufrufe einer dieser Methoden geben MAPI_E_INVALID_OBJECT. Die **Verwendung von MakeInvalid** ist eine Option, die viele Dienstanbieter ignorieren. 
  
## <a name="see-also"></a>Siehe auch



[Herunterfahren eines Dienstanbieters](shutting-down-a-service-provider.md)

