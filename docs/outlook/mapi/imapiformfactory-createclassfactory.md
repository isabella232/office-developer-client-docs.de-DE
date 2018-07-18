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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 823e10a1f496f5f5e8bab00f94d700d06e753b48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792170"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**Betrifft**: Outlook 
  
Gibt ein Klasse Factory-Objekt für das Formular.
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>Parameter

 _clsidForm_
  
> [in] Eine Klassen-ID für das Formular von der Klassenfactory erstellt werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lppClassFactory_
  
> [out] Ein Zeiger auf das Klassenobjekt Factory.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Klassenobjekt Factory wurde zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Formular Viewer rufen Sie die **IMAPIFormFactory::CreateClassFactory** -Methode, um eine Klassenfactory für ein bestimmtes Formular zu erhalten. Die ClassFactory wird verwendet, um Instanzen eines Formulars zu erstellen, die Nachrichten von einer bestimmten Klasse behandelt und den Zugriff auf diese Instanzen steuern. 
  
Die **CreateClassFactory** -Methode wird von Formular Zuschauer zu einer Factory Klassenobjekt für Formular-Server abzurufen, die mehrere Nachrichtenklassen implementieren aufgerufen. Diese Methode empfängt eine Klassen-ID (CLSID) als Parameter. Basierend auf diesen Parameter, kann diese Methode die Art des zurückzugebenden Klassenfactoryobjekts-Factory bestimmen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können aus der **CreateClassFactory** -Implementierung das gleiche Factory Klassenobjekt auf mehrere Aufrufe für die gleichen Klassen-ID zurückgeben. Erstellen einer neuen Instanz der Klasse Factory ist nicht erforderlich. 
  
Sie können eine einzelne Klasse Factory-Implementierung, die Instanzen der entsprechenden Factory bei Bedarf erstellt oder mehrere Klasse Factory Implementierungen für jede Nachrichtenklasse haben.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

