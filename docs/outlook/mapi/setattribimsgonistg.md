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
  
Legt Attribute von Eigenschaften für ein [IMessage](imessageimapiprop.md) -Objekt fest, das von der [OpenIMsgOnIStg](openimsgonistg.md) -Funktion bereitgestellt wird, oder ändert Sie. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Nachrichtenspeicher Anbieter  <br/> |
   
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
  
> in Zeiger auf das Objekt, für das Eigenschaftsattribute festgelegt werden. 
    
 _lpPropTags_
  
> in Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags angibt, die die Eigenschaften angeben, für die Eigenschaftsattribute festgelegt werden. 
    
 _lpPropAttrs_
  
> in Zeiger auf eine [SPropAttrArray](spropattrarray.md) -Struktur, die die festzulegenden Eigenschaften Attribute auflistet. 
    
 _lppPropProblems_
  
> Out Zeiger auf die zurückgegebene [SPropProblemArray](spropproblemarray.md) -Struktur mit einem Satz von Eigenschafts Problemen. Diese Struktur identifiziert Probleme, die auftreten, wenn **SetAttribIMsgOnIStg** einige Eigenschaften festlegen konnte, aber nicht alle. Wenn ein Zeiger auf NULL im _lppPropProblems_ -Parameter übergeben wird, wird kein Eigenschaften Problem Array zurückgegeben, auch wenn einige Eigenschaften nicht festgelegt wurden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber auf eine oder mehrere Eigenschaften konnte nicht zugegriffen werden, und es wurde ein Eigenschaftentyp von PT_ERROR zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Auf Eigenschaftsattribute kann nur über Property-Objekte zugegriffen werden, also auf Objekte, die die [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle implementieren. Um MAPI-Eigenschaften für ein OLE Structured Storage-Objekt verfügbar zu machen, erstellt [OpenIMsgOnIStg](openimsgonistg.md) ein [IMessage: IMAPIProp](imessageimapiprop.md) -Objekt über dem OLE- **IStorage** -Objekt. Die Eigenschaftsattribute für solche Objekte können mit **SetAttribIMsgOnIStg** festgelegt oder geändert und mit [GetAttribIMsgOnIStg](getattribimsgonistg.md)abgerufen werden. 
  
 **Hinweis** **GetAttribIMsgOnIStg** und **SetAttribIMsgOnIStg** funktionieren nicht für alle **IMessage** -Objekte. Sie sind nur für **IMessage**-on- **IStorage** -Objekte gültig, die von **OpenIMsgOnIStg**zurückgegeben werden. 
  
Im _lpPropAttrs_ -Parameter müssen die Anzahl und die Position der Attribute mit der Anzahl und Position der im _lpPropTags_ -Parameter übergebenen Property-Tags übereinstimmen. 
  
Die **SetAttribIMsgOnIStg** -Funktion wird verwendet, um Nachrichteneigenschaften schreibgeschützt zu machen, wenn Sie vom **IMessage** -Schema benötigt werden. Der Beispiel-Nachrichtenspeicher Anbieter verwendet diesen zu diesem Zweck. Weitere Informationen finden Sie unter [Nachrichten](mapi-messages.md). 
  

