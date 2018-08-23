---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3d78b4e6a4a0cc3363edefc84e7ae80dbe72c510
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590358"
---
# <a name="wizardentry"></a>WIZARDENTRY

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Definiert eine Funktion Service Provider Eintrag Punkt, der der Profil-Assistent zurückruft ausreichend Informationen zum Anzeigen des Anbieters Konfiguration-Eigenschaftenblätter abgerufen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiwz.h  <br/> |
|Definierte Funktion von implementiert:  <br/> |Dienstanbieter  <br/> |
|Definierte Funktion aufgerufen:  <br/> |MAPI-Profil-Assistent  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a>Parameter

 _hProviderDLLInstance_
  
> [in] Instanzzugriffsnummer der DLL des Dienstanbieters. 
    
 _lpcsResourceName_
  
> [out] Zeiger auf eine Zeichenfolge, die den vollständigen Namen der die Ressource enthält, die während der Konfiguration von der Profil-Assistent angezeigt werden sollen. Die maximale Größe der Zeichenfolge, einschließlich der NULL-Terminator beträgt 32 Zeichen. 
    
 _lppDlgProc_
  
> [out] Zeiger auf eine standard Windows Dialogfeld Feld Prozedur, die mithilfe des Profil-Assistenten, um die Anbieter von verschiedenen Ereignisse benachrichtigen aufgerufen wird. 
    
 _lpMAPIProp_
  
> [in] Zeiger auf eine Implementierung der Eigenschaft-Schnittstelle, die Zugriff auf die Konfigurationseigenschaften bereitstellt. 
    
 _lpMapiSupportObject_
  
> [in] Zeiger auf das Objekt der MAPI-Unterstützung für diese Sitzung gelten.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Dienstanbieter **WIZARDENTRY** Funktion wurde erfolgreich aufgerufen. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler unerwartete oder unbekannten Ursprungs verhindert den Abschluss des Vorgangs.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der Profil-Assistent Ruft die **WIZARDENTRY** Basis-Funktion, wenn der Dienstanbieter Konfigurationsbenutzeroberfläche anzeigen kann. Nach Abschluss der Profil-Assistent alle Anbieter konfigurieren, werden die Konfigurationseigenschaften auf das Profil durch Aufrufen von [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)schreibt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Name der Funktion **WIZARDENTRY** basierend muss im Eintrag WIZARD_ENTRY_NAME MAPISVC.INF platziert werden. 
  
Der Ressourcenname ist, der die Ressource, die im Bereich des Assistenten Profil gerendert wird. Die Ressource, die Back muss alle Seiten in einer einzelnen Ressource enthalten übergeben wird. Wenn der Profil-Assistent diese Ressource empfängt, wird das Dialogfeld Formatvorlage, aber nicht die Steuerelement-Formatvorlagen ignoriert, und alle Steuerelemente als untergeordnete Elemente des der Profil-Assistent-Seite erstellt. Alle Steuerelemente sind anfangs ausgeblendet. Anbieter sollte stellen Sie sicher, dass die Koordinaten für die Steuerelemente auf 0 (null) sind oder nullbasierte und, dass sie eine maximale Breite von 200 Dialogfeld Einheiten und eine maximale Höhe von 150 Dialogfeld Einheiten nicht überschreiten. Steuerelement-IDs unter 400 sind für das Profil-Assistent reserviert. Der Profil-Assistent des Anbieters Titel in Fettschrift oberhalb des Anbieters-Benutzeroberfläche angezeigt. 
  
Eigenschaft Schnittstellenzeiger im _LpMAPIProp_ -Parameter sollte vom Anbieter für die zukünftige beibehalten werden. Der Profil-Assistent befasst sich mit den grundlegenden Satz Eigenschaften, und der Anbieter kann die Implementierung der Eigenschaft-Schnittstelle verwenden, um zusätzliche Eigenschaften gehören. Während der Konfiguration sollten Anbieter ihre Konfigurationseigenschaften auf das Objekt, das die Eigenschaft-Schnittstelle implementieren hinzuzufügen. Nachdem alle Anbieter konfiguriert wurden, fügt der Profil-Assistent diese Eigenschaften auf das Profil. 
  
Weitere Informationen zu dieser Funktion finden Sie unter [Message-Dienstkonfiguration unterstützen](supporting-message-service-configuration.md). 
  

