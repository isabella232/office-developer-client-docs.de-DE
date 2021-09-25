---
title: IMAPIFormInfoMakeIconFromBinary
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormInfo.MakeIconFromBinary
api_type:
- COM
ms.assetid: 4daeddd7-3f0c-4178-ae8d-f74814090d40
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 813c76d2c4d81dd50760fc356c2af6f8cc41054e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567585"
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
  
> [in] Ein Eigenschaftsbezeichner für eine Symboleigenschaft.
    
 _Phicon_
  
> [out] Ein Zeiger auf das zurückgegebene Symbol.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Clientanwendungen rufen die **IMAPIFormInfo::MakeIconFromBinary-Methode** auf, um ein Symbol aus einer der Symboleigenschaften eines Formulars zu erstellen. Im  _Parameter nPropID_ verwendet **MakeIconFromBinary** den Eigenschaftenbezeichner einer der Symboleigenschaften eines Formulars. Mithilfe dieses Eigenschaftsbezeichners wird ein Symbol erstellt, das in Tabellenansichten angezeigt werden kann, die Eigenschaftsspalten für Symbole enthalten. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

