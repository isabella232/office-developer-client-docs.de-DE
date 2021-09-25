---
title: Ungültige Gültigkeit eines Objekts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 28db490d9acff055705fc75ff2d45741ddf651fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571640"
---
# <a name="invalidating-an-object"></a>Ungültige Gültigkeit eines Objekts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im Rahmen des Herunterfahrens Ihres Anbieters möchten Sie möglicherweise ein Objekt ungültig machen. Für die Ungültigerklärung eines Objekts wird die vtable durch eine vtable ersetzt, die Implementierungen für die drei **IUnknown** -Methoden enthält: **AddRef**, **Release** und **QueryInterface**. Ungültigmachen eines Objekts durch Aufrufen von [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), einer Methode, die im Supportobjekt jedes der drei allgemeinen Anbietertypen enthalten ist. Anbieter führen diesen Aufruf in der Regel in der Implementierung der **Logoff-Methode** ihres Anmeldeobjekts durch. 
  
Die Ungültigkeit eines Objekts gibt der MAPI die letzte Verantwortung für die Freigabe des einem Objekt zugeordneten Speichers. Sie können alle Ressourcen freigeben, die mit einem Objekt verbunden sind, und dann **MakeInvalid** aufrufen, um alle Methoden in den geerbten Schnittstellen ungültig zu machen. Aufrufe dieser Methoden geben MAPI_E_INVALID_OBJECT zurück. Die Verwendung von **MakeInvalid** ist eine Option, die von vielen Dienstanbietern ignoriert werden soll. 
  
## <a name="see-also"></a>Siehe auch



[Herunterfahren eines Dienstanbieters](shutting-down-a-service-provider.md)

