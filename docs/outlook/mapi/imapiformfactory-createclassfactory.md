---
title: IMAPIFormFactoryCreateClassFactory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormFactory.CreateClassFactory
api_type:
- COM
ms.assetid: dceb21b1-be5e-418d-b0c9-db39195fc82e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 69b371f5fda78159ff3626148cbc6ef32370a263
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551352"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein Klassenfactoryobjekt für das Formular zurück.
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>Parameter

 _clsidForm_
  
> [in] Ein Klassenbezeichner für das Formular, das von der Klassenfactory erstellt werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lppClassFactory_
  
> [out] Ein Zeiger auf das Klassenfactoryobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Klassenfactoryobjekt wurde zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIFormFactory::CreateClassFactory-Methode** auf, um eine Klassenfactory für ein bestimmtes Formular abzurufen. Die Klassenfactory wird verwendet, um Instanzen eines Formulars zu erstellen, das Nachrichten einer bestimmten Klasse verarbeitet, und um den Zugriff auf diese Instanzen zu steuern. 
  
Die **CreateClassFactory-Methode** wird von Formularviewern aufgerufen, um ein Klassenfactoryobjekt für Formularserver abzurufen, die mehrere Nachrichtenklassen implementieren. Diese Methode empfängt einen Klassenbezeichner (CLSID) als Parameter. Basierend auf diesem Parameter kann diese Methode die spezifische Art des zurückzugebenden Klassenfactoryobjekts bestimmen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können von der **CreateClassFactory-Implementierung** dasselbe Klassenfactoryobjekt bei mehreren Aufrufen desselben Klassenbezeichners zurückgeben. Das Erstellen einer neuen Klassenfactoryinstanz ist nicht erforderlich. 
  
Sie können über eine einzelne Klassenfactoryimplementierung verfügen, die bei Bedarf geeignete Klassenfactoryinstanzen erstellt, oder mehrere Klassenfactoryimplementierungen, eine für jede Nachrichtenklasse.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

