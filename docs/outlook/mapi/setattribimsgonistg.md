---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 852ce31ba5ab02ff8f05dee25c9b32acb73130ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428830"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt Attribute von Eigenschaften für ein [IMessage-Objekt](imessageimapiprop.md) fest, das von der [OpenIMsgOnIStg-Funktion bereitgestellt](openimsgonistg.md) wird, oder ändert sie. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Imessage.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Nachrichtenspeicheranbieter  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a>Parameter

 _lpObject_
  
> [in] Zeiger auf das Objekt, für das Eigenschaftenattribute festgelegt werden. 
    
 _lpPropTags_
  
> [in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die die Eigenschaften angeben, für die Eigenschaftenattribute festgelegt werden. 
    
 _lpPropAttrs_
  
> [in] Zeiger auf eine [SPropAttrArray-Struktur,](spropattrarray.md) die die festgelegten Eigenschaftenattribute auflistet. 
    
 _lppPropProblems_
  
> [out] Zeiger auf die zurückgegebene [SPropProblemArray-Struktur](spropproblemarray.md) mit einer Reihe von Eigenschaftsproblemen. Diese Struktur identifiziert Probleme, die **auftreten, wenn SetAttribIMsgOnIStg** einige Eigenschaften festlegen konnte, aber nicht alle. Wenn ein Zeiger auf NULL im  _lppPropProblems-Parameter_ übergeben wird, wird kein Eigenschaftsproblemarray zurückgegeben, auch wenn einige Eigenschaften nicht festgelegt wurden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber auf eine oder mehrere Eigenschaften konnte nicht zugegriffen werden und wurde mit dem Eigenschaftstyp PT_ERROR.
    
## <a name="remarks"></a>Hinweise

Auf Eigenschaftsattribute kann nur auf Eigenschaftsobjekte zugegriffen werden, d. h. auf Objekte, die die [IMAPIProp : IUnknown-Schnittstelle](imapipropiunknown.md) implementieren. Um MAPI-Eigenschaften für ein strukturiertes OLE-Speicherobjekt verfügbar zu machen, erstellt [OpenIMsgOnIStg](openimsgonistg.md) ein [IMessage : IMAPIProp-Objekt](imessageimapiprop.md) über dem OLE **IStorage-Objekt.** Die Eigenschaftenattribute für solche Objekte können mit **SetAttribIMsgOnIStg** festgelegt oder geändert und mit [GetAttribIMsgOnIStg abgerufen werden.](getattribimsgonistg.md) 
  
 **Hinweis** **GetAttribIMsgOnIStg** und **SetAttribIMsgOnIStg** funktionieren nicht für alle **IMessage-Objekte.** Sie sind nur gültig für **IMessage** **-on-IStorage-Objekte,** die von **OpenIMsgOnIStg zurückgegeben werden.** 
  
Im  _lpPropAttrs-Parameter_ müssen Anzahl und Position der Attribute mit der Anzahl und Position der Eigenschaftstags übereinstimmen, die im  _lpPropTags-Parameter übergeben_ werden. 
  
Die **SetAttribIMsgOnIStg-Funktion** wird verwendet, um Nachrichteneigenschaften schreibgeschützt zu machen, wenn dies im **IMessage-Schema erforderlich** ist. Der Beispielnachrichtenspeicheranbieter verwendet ihn zu diesem Zweck. Weitere Informationen finden Sie unter [Nachrichten](mapi-messages.md). 
  

