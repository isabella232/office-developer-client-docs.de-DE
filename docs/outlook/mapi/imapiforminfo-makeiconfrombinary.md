---
title: IMAPIFormInfoMakeIconFromBinary
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.MakeIconFromBinary
api_type:
- COM
ms.assetid: 4daeddd7-3f0c-4178-ae8d-f74814090d40
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 30f55044327eecee3ab0d8ee2509d7132ab6e8ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570128"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erstellt ein Symbol aus der Symboleigenschaften eines Formulars an.
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>Parameter

 _nPropID_
  
> [in] Ein Bezeichner für ein Icon-Eigenschaft.
    
 _phicon_
  
> [out] Ein Zeiger auf das zurückgegebene Symbol.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Clientanwendungen rufen Sie die **IMAPIFormInfo::MakeIconFromBinary** -Methode, um ein Symbol aus der Symboleigenschaften eines Formulars zu erstellen. In den _nPropID_ -Parameter akzeptiert **MakeIconFromBinary** der Bezeichner der der Symboleigenschaften eines Formulars. Mit dieser Eigenschaftenbezeichner, erstellt er ein Symbol, das in der Tabelle angezeigt werden kann, die Eigenschaftenspalten für Symbole enthalten. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

