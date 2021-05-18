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
ms.openlocfilehash: 418056f7222d5ab05f43a3661c1811bf2ae15be8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405114"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt ein Symbol aus einer der Symboleigenschaften eines Formulars.
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>Parameter

 _nPropID_
  
> [in] Eine Eigenschafts-ID für eine Icon-Eigenschaft.
    
 _phicon_
  
> [out] Ein Zeiger auf das zurückgegebene Symbol.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Clientanwendungen rufen die **IMAPIFormInfo::MakeIconFromBinary-Methode** auf, um ein Symbol aus einer der Symboleigenschaften eines Formulars zu erstellen. Im  _Parameter nPropID_ übernimmt **MakeIconFromBinary** die Eigenschafts-ID einer der Symboleigenschaften eines Formulars. Mithilfe dieser Eigenschafts-ID wird ein Symbol erstellt, das in Tabellenansichten angezeigt werden kann, die Eigenschaftenspalten für Symbole enthalten. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

