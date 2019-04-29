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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: babff746af16d51ca154d049943f6be7e9fab589
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428781"
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
  
> in Eine Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
 _ppMAPIVerbArray_
  
> Out Ein Zeiger auf einen Zeiger auf die zurückgegebene [SMAPIVerbArray](smapiverbarray.md) -Struktur, die die Verben des Formulars enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Bemerkungen

Client Anwendungen rufen die **IMAPIFormInfo:: CalcVerbSet** -Methode auf, um einen Zeiger auf die von einem Formular verwendete Verben abzurufen. In der **SMAPIVerbArray** -Struktur, die im Parameter _ppMAPIVerbArray_ zurückgegeben wird, werden die Verben in der Reihenfolge der Indexnummer zurückgegeben. jeder Verb Index wird im **lVerb** -Element gefunden. Client Anwendungen können das Verb-Array verwenden, um Menüs dynamisch zu erstellen, Schaltflächen ein-oder auszublenden usw. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MFCOutput. cpp  <br/> |_OutputFormInfo  <br/> |MFCMAPI verwendet die **IMAPIFormInfo:: CalcVerbSet** -Methode beim Schreiben der Debug-Ausgabe für Formular Informationsobjekte.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SMAPIVerbArray](smapiverbarray.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

