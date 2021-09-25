---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a6f7dd8c8e583841b6805a4dd0416703d79c087b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578655"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt die Attribute von Eigenschaften für ein [IMessage-Objekt](imessageimapiprop.md) fest, das von der [OpenIMsgOnIStg-Funktion](openimsgonistg.md) bereitgestellt wird, oder ändert diese. 
  
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
  
> [in] Zeiger auf das Objekt, für das Eigenschaftsattribute festgelegt werden. 
    
 _lpPropTags_
  
> [in] Zeiger auf eine [SPropTagArray-Struktur](sproptagarray.md) mit einem Array von Eigenschaftstags, das die Eigenschaften angibt, für die Eigenschaftsattribute festgelegt werden. 
    
 _lpPropAttrs_
  
> [in] Zeiger auf eine [SPropAttrArray-Struktur,](spropattrarray.md) die die festzulegenden Eigenschaftsattribute auflistet. 
    
 _lppPropProblems_
  
> [out] Zeiger auf die zurückgegebene [SPropProblemArray-Struktur,](spropproblemarray.md) die eine Reihe von Eigenschaftsproblemen enthält. Diese Struktur identifiziert Probleme, die auftreten, wenn **SetAttribIMsgOnIStg** einige Eigenschaften festlegen konnte, aber nicht alle. Wenn im  _Parameter "lppPropProblems"_ ein Zeiger auf NULL übergeben wird, wird auch dann kein Eigenschaftsproblemarray zurückgegeben, wenn einige Eigenschaften nicht festgelegt wurden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber auf eine oder mehrere Eigenschaften konnte nicht zugegriffen werden und wurde mit einem Eigenschaftentyp von PT_ERROR zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Auf Eigenschaftsattribute kann nur auf Eigenschaftsobjekte zugegriffen werden, d. h. auf Objekte, die die [IMAPIProp : IUnknown-Schnittstelle](imapipropiunknown.md) implementieren. Um MAPI-Eigenschaften für ein strukturiertes OLE-Speicherobjekt verfügbar zu machen, erstellt [OpenIMsgOnIStg](openimsgonistg.md) ein [IMessage : IMAPIProp-Objekt](imessageimapiprop.md) über dem OLE **IStorage-Objekt.** Die Eigenschaftsattribute für solche Objekte können mit **SetAttribIMsgOnIStg** festgelegt oder geändert und mit [GetAttribIMsgOnIStg](getattribimsgonistg.md)abgerufen werden. 
  
 **Hinweis:** **GetAttribIMsgOnIStg** und **SetAttribIMsgOnIStg** funktionieren nicht für alle **IMessage-Objekte.** Sie sind nur gültig für **IMessage**-on- **IStorage-Objekte,** die von **OpenIMsgOnIStg** zurückgegeben werden. 
  
Im  _Parameter lpPropAttrs_ müssen die Anzahl und Position der Attribute mit der Anzahl und Position der Eigenschaftentags übereinstimmen, die im  _lpPropTags-Parameter_ übergeben werden. 
  
Die **SetAttribIMsgOnIStg-Funktion** wird verwendet, um Nachrichteneigenschaften schreibgeschützt zu machen, wenn dies für das **IMessage-Schema** erforderlich ist. Der Beispielanbieter für den Nachrichtenspeicher verwendet ihn für diesen Zweck. Weitere Informationen finden Sie unter [Nachrichten](mapi-messages.md). 
  

