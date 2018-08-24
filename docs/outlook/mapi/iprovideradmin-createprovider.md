---
title: IProviderAdminCreateProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.CreateProvider
api_type:
- COM
ms.assetid: 80c1449a-6cd9-4b93-a300-395979894b71
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f76b44b3718f08eb68fc956ad4480d4327cb0656
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578626"
---
# <a name="iprovideradmincreateprovider"></a>IProviderAdmin::CreateProvider

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt einen Dienstanbieter an den Dienst. 
  
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
  
> [in] Ein Zeiger auf den Namen des hinzuzufügenden Anbieters an.
    
 _cValues_
  
> [in] Die Anzahl der Eigenschaftswerte, die auf den durch den Parameter _LpProps_ verwiesen. 
    
 _lpProps_
  
> [in] Ein Zeiger auf ein Array-Eigenschaft Wert, der beschreibt die Eigenschaften des hinzuzufügenden Anbieters an.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster des alle Dialogfelder oder Fenster zeigt diese Methode an. Der Parameter _UlUIParam_ wird verwendet, wenn das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die die hinzugefügte Anbieter steuert. Die folgenden Kennzeichen können festgelegt werden:
    
  - MAPI_DIALOG: Zeigt ein Dialogfeld Informationen zur Konfiguration aufgefordert.
      
  - Parameter MAPI_UNICODE: Anbieter für die Eigenschaften Name und die Zeichenfolge sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind diese Zeichenfolgen in ANSI-Format.
    
 _lpUID_
  
> [out] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner, der den Anbieter enthält hinzufügen darstellt. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Anbieter wurde erfolgreich an den Nachrichtendienst hinzugefügt.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen. 
    
## <a name="remarks"></a>Bemerkungen

Die **IProviderAdmin::CreateProvider** -Methode hinzugefügt der Messagingdiensts einen Dienstanbieter. Der Parameter _LpszProvider_ muss auf den Namen eines Anbieters zeigen, die den Dienst gehört. **CreateProvider** überprüft nicht, ob der Name des Anbieters in den Dienst mit dem Namen übereinstimmt; Wenn der übergebene Name den Namen eines Dienstes nicht übereinstimmt, der Aufruf erfolgreich ist, aber sind die Ergebnisse unvorhersehbar. Die meisten Message-Dienste können nicht Anbieter hinzugefügt oder gelöscht werden, während das Profil verwendet wird. 
  
Nachdem alle verfügbaren Informationen über den Dienst wurde Anbieter hinzugefügt das Profil aus der Datei "Mapisvc.inf" **CreateProvider** die Messagingdiensts Eintrag Punkt mit der _UlContext_ -Parameter auf MSG_SERVICE_ Funktionsaufrufe PROVIDER_CREATE. Wenn in der **CreateProvider** -Methode _UlFlags_ Parameter MAPI_DIALOG festgelegt ist, werden die Werte in den _UlUIParam_ und _UlFlags_ auch an die Eintrags-Funktion übergeben. Aktivieren Sie diese zusätzlichen Parameter des-Dienstanbieters für das Eigenschaftenfenster anzuzeigen, damit der Benutzer Konfigurationseinstellungen eingeben kann. 
  
## <a name="see-also"></a>Siehe auch

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

