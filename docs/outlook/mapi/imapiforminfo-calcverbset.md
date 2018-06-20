---
title: IMAPIFormInfoCalcVerbSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 362afb1efeddeae72cc19256c377cb2c0f7ecba0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792163"
---
# <a name="imapiforminfocalcverbset"></a>IMAPIFormInfo::CalcVerbSet

  
  
**Betrifft**: Outlook 
  
Gibt einen Zeiger auf den vollständigen Satz von Verben, die ein Formular verwendet wird.
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 _ppMAPIVerbArray_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene [SMAPIVerbArray](smapiverbarray.md) -Struktur, die dem Formular zugrunde Verben enthält. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Hinweise

Clientanwendungen rufen Sie die **IMAPIFormInfo::CalcVerbSet** -Methode, um einen Zeiger auf den Satz von Verben, die von einem Formular verwendeten abrufen. In der **SMAPIVerbArray** -Struktur, die in der _PpMAPIVerbArray_ -Parameter zurückgegeben werden die Verben in der Reihenfolge der Indexnummer zurückgegeben. Index des Verbs wird in seinem **lVerb** Mitglied gefunden. Clientanwendungen können das Verb Array dynamisch erstellen Menüs, ausblenden oder Schaltflächen anzeigen, und so weiter. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MFCOutput.cpp  <br/> |_OutputFormInfo  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFormInfo::CalcVerbSet** -Methode beim Schreiben der Debugausgabe für Formular Informationen-Objekte.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SMAPIVerbArray](smapiverbarray.md)
  
[IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

