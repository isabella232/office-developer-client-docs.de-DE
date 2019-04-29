---
title: Invalidieren eines Objekts
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
# <a name="invalidating-an-object"></a>Invalidieren eines Objekts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im Rahmen des Herunterfahrens des Anbieters möchten Sie möglicherweise ein Objekt ungültig machen. Für die Invalidierung eines Objekts wird die Vtable durch eine Vtable ersetzt, die Implementierungen für die drei **IUnknown** -Methoden enthält: **AddRef**, **Release**und **QueryInterface**. Ein Objekt wird ungültig, indem [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md), eine Methode aufgerufen wird, die im Support Objekt der drei gängigen Anbietertypen enthalten ist. Anbieter führen diesen Aufruf in der Regel in der Implementierung der **Logout** -Methode Ihres LOGON-Objekts aus. 
  
Durch die Invalidierung eines Objekts wird MAPI die ultimative Verantwortung für die Freigabe des Arbeitsspeichers zugewiesen, der einem Objekt zugeordnet ist. Sie können alle mit einem Objekt verbundenen Ressourcen freigeben und dann **MakeInvalid** aufrufen, um alle Methoden in den geerbten Schnittstellen zu invalidieren. Aufrufe einer dieser Methoden geben MAPI_E_INVALID_OBJECT zurück. Die Verwendung von **MakeInvalid** ist eine Option, die von vielen Dienstanbietern ignoriert werden kann. 
  
## <a name="see-also"></a>Siehe auch



[Herunterfahren eines Dienstanbieters](shutting-down-a-service-provider.md)

