---
title: IProviderAdminCreateProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProviderAdmin.CreateProvider
api_type:
- COM
ms.assetid: 80c1449a-6cd9-4b93-a300-395979894b71
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf8ec09bc58934e9fb4195a3bd838dc2d7f849df
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592263"
---
# <a name="iprovideradmincreateprovider"></a>IProviderAdmin::CreateProvider

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt dem Nachrichtendienst einen Dienstanbieter hinzu. 
  
```cpp
HRESULT CreateProvider(
  LPSTR lpszProvider,
  ULONG cValues,
  LPSPropValue lpProps,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  MAPIUID FAR * lpUID
);
```

## <a name="parameters"></a>Parameter

 _lpszProvider_
  
> [in] Ein Zeiger auf den Namen des hinzuzufügenden Anbieters.
    
 _cValues_
  
> [in] Die Anzahl der Eigenschaftswerte, auf die der  _lpProps-Parameter_ verweist. 
    
 _lpProps_
  
> [in] Ein Zeiger auf ein Eigenschaftswertarray, das die Eigenschaften des hinzuzufügenden Anbieters beschreibt.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden. Der  _ulUIParam-Parameter_ wird verwendet, wenn das MAPI_DIALOG-Flag im  _ulFlags-Parameter_ festgelegt ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die das Hinzufügen des Anbieters steuert. Die folgenden Flags können festgelegt werden:
    
  - MAPI_DIALOG: Zeigt ein Dialogfeld an, in dem Sie zur Eingabe von Konfigurationsinformationen aufgefordert werden.
      
  - MAPI_UNICODE: Der Anbietername und die Zeichenfolgeneigenschaften haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben diese Zeichenfolgen das ANSI-Format.
    
 _lpUID_
  
> [out] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner enthält, der den hinzuzufügenden Anbieter darstellt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Anbieter wurde dem Nachrichtendienst erfolgreich hinzugefügt.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** in einem Dialogfeld. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IProviderAdmin::CreateProvider-Methode** fügt dem Nachrichtendienst einen Dienstanbieter hinzu. Der  _parameter lpszProvider_ muss auf den Namen eines Anbieters verweisen, der zum Nachrichtendienst gehört. **CreateProvider** überprüft nicht, ob der Name mit dem Namen eines Anbieters im Dienst übereinstimmt. wenn der übergebene Name nicht mit einem Dienstnamen übereinstimmt, ist der Aufruf erfolgreich, aber die Ergebnisse sind unvorhersehbar. Die meisten Nachrichtendienste lassen nicht zu, dass Anbieter hinzugefügt oder gelöscht werden, während das Profil verwendet wird. 
  
Nachdem alle verfügbaren Informationen zum Dienstanbieter dem Profil aus der Datei Mapisvc.inf hinzugefügt wurden, ruft **CreateProvider** die Einstiegspunktfunktion des Nachrichtendiensts auf, wobei der  _ulContext-Parameter_ auf MSG_SERVICE_PROVIDER_CREATE festgelegt ist. Wenn MAPI_DIALOG im _ulFlags-Parameter_ der **CreateProvider-Methode** festgelegt ist, werden auch die Werte in den _Parametern ulUIParam_ und _ulFlags_ an die Einstiegspunktfunktion übergeben. Mit diesen zusätzlichen Parametern kann der Dienstanbieter sein Eigenschaftenblatt anzeigen, damit der Benutzer Konfigurationseinstellungen eingeben kann. 
  
## <a name="see-also"></a>Siehe auch

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

