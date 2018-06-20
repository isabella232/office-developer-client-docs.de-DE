---
title: Ein Objekt ungültig
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9c0ba8f1f0bf31bb892f380df310cd9fa7a8a24f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792716"
---
# <a name="invalidating-an-object"></a>Ein Objekt ungültig

  
  
**Betrifft**: Outlook 
  
Als Teil des Herunterfahrens des Anbieters sollten Sie ein Objekt ungültig. Ein Objekt ungültig umfasst, und Ersetzen Sie die vtable des Objekts durch eine Vtable, die Implementierungen für die drei **IUnknown** -Methoden enthält: **QueryInterface**, **AddRef**und **Release**. Ein Objekt ungültig wird durch Aufrufen von [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), eine Methode, die im jedes der drei allgemeine Providertypen Support-Objekt enthalten ist. Anbieter stellen dieses Anrufs in der Regel in der Implementierung von ihrer Anmeldung-Objekt **Logoff (** Methode). 
  
Ein Objekt ungültig bietet MAPI die ultimative Verantwortung für ein Objekt zugeordneten Arbeitsspeicher freizugeben. Sie können alle Ressourcen verbunden mit einem Objekt frei, und rufen Sie dann **MakeInvalid** , um alle Methoden in seiner geerbten Schnittstellen ungültig. Anrufe an eine der folgenden Methoden gibt MAPI_E_INVALID_OBJECT zurück. Verwenden von **MakeInvalid** ist eine Option, die viele Dienstanbieter ignoriert werden sollen. 
  
## <a name="see-also"></a>Siehe auch



[Herunterfahren von einem Dienstanbieter](shutting-down-a-service-provider.md)

