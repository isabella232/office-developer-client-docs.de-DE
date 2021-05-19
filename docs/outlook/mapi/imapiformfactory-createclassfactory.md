---
title: IMAPIFormFactoryCreateClassFactory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.CreateClassFactory
api_type:
- COM
ms.assetid: dceb21b1-be5e-418d-b0c9-db39195fc82e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6e616a76d9665b602184e88566384506fcce5697
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416076"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein Klassen factory-Objekt für das Formular zurück.
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>Parameter

 _clsidForm_
  
> [in] Ein Klassenbezeichner für das Formular, das von der Klassen factory erstellt werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lppClassFactory_
  
> [out] Ein Zeiger auf das Klassen factory-Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Klassen factory-Objekt wurde zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIFormFactory::CreateClassFactory-Methode** auf, um eine Klassen factory für ein bestimmtes Formular zu erhalten. Die Klassen factory wird verwendet, um Instanzen eines Formulars zu erstellen, das Nachrichten einer bestimmten Klasse verarbeitet, und um den Zugriff auf diese Instanzen zu steuern. 
  
Die **CreateClassFactory-Methode** wird von Formularanzeigen aufgerufen, um ein Klassen factory-Objekt für Formularserver zu erhalten, die mehrere Nachrichtenklassen implementieren. Diese Methode empfängt eine Klassen-ID (CLSID) als Parameter. Basierend auf diesem Parameter kann diese Methode die spezifische Art des zurückgebenden Klassen factory-Objekts bestimmen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können von Ihrer **CreateClassFactory-Implementierung** dasselbe Klassen factory-Objekt bei mehreren Aufrufen für denselben Klassenbezeichner zurückgeben. Das Erstellen einer neuen Klassen factory-Instanz ist nicht erforderlich. 
  
Sie können über eine einzelne Factoryimplementierung einer Klasse verfügen, mit der bei Bedarf geeignete Klassen factory-Instanzen oder mehrere Factoryimplementierungsklassen einer Klasse für jede Nachrichtenklasse erstellt werden.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

