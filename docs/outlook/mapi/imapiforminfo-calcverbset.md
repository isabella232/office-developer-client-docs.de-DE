---
title: IMAPIFormInfoCalcVerbSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9c7ecf9ae44cb19c6040b713fe77cfb6cf44a066
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551289"
---
# <a name="imapiforminfocalcverbset"></a>IMAPIFormInfo::CalcVerbSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeiger auf den vollständigen Satz von Verben zurück, die ein Formular verwendet.
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 _ppMAPIVerbArray_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene [SMAPIVerbArray-Struktur,](smapiverbarray.md) die die Verben des Formulars enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>HinwBemerkungeneise

Clientanwendungen rufen die **IMAPIFormInfo::CalcVerbSet-Methode** auf, um einen Zeiger auf die von einem Formular verwendete Gruppe von Verben abzurufen. In der **SMAPIVerbArray-Struktur,** die im _PpMAPIVerbArray-Parameter_ zurückgegeben wird, werden die Verben in der Reihenfolge der Indexnummer zurückgegeben. Der Index jedes Verbs befindet sich in seinem **lVerb-Element.** Clientanwendungen können das Verbarray verwenden, um Menüs dynamisch zu erstellen, Schaltflächen auszublenden oder anzuzeigen usw. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MFCOutput.cpp  <br/> |_OutputFormInfo  <br/> |MFCMAPI verwendet die **IMAPIFormInfo::CalcVerbSet-Methode** beim Schreiben der Debugausgabe für Formularinformationsobjekte.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SMAPIVerbArray](smapiverbarray.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

