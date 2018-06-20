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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a230e8b69a64646dffb23147345d5960fdd38581
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792165"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**Betrifft**: Outlook 
  
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



[IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md)

