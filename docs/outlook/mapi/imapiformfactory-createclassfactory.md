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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342175"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein klassenfactoryobjekt für das Formular zurück.
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>Parameter

 _clsidForm_
  
> in Ein Klassenbezeichner für das Formular, das von der Klassenfactory erstellt werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lppClassFactory_
  
> Out Ein Zeiger auf das Klassenfactory-Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Klassenfactory-Objekt wurde zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IMAPIFormFactory:: CreateClassFactory** -Methode auf, um eine Klassenfactory für ein bestimmtes Formular abzurufen. Die Class Factory wird verwendet, um Instanzen eines Formulars zu erstellen, das Nachrichten einer bestimmten Klasse verarbeitet und den Zugriff auf diese Instanzen steuert. 
  
Die **CreateClassFactory** -Methode wird von Formular Viewern aufgerufen, um ein klassenfactoryobjekt für Formularserver abzurufen, die mehrere Nachrichtenklassen implementieren. Diese Methode empfängt eine Klassen-ID (CLSID) als Parameter. Anhand dieses Parameters kann diese Methode die spezifische Art des zurückzugebenden Klassenfactory-Objekts bestimmen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können von der **CreateClassFactory** -Implementierung das gleiche Klassenfactory-Objekt für mehrere Aufrufe für denselben Klassenbezeichner zurückgeben. Das Erstellen einer neuen Klassenfactory-Instanz ist nicht erforderlich. 
  
Sie können eine einzelne Klasse Factory-Implementierung haben, die entsprechende Klassen Factory-Instanzen bei Bedarf erstellt, oder mehrere Klassenfactory-Implementierungen, eine für jede Nachrichtenklasse.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

