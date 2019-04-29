---
title: Bereitstellen signierter InfoPath-Formularvorlagen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8345a4bc-ad7b-d0b0-7615-f77ade35006d
description: Bevor Sie dieses Thema lesen, finden Sie unter theSigned Form Templatessection in zusätzlichen InfoPath-Formular Sicherheitskonzepte Informationen zur Sicherheit signierter Formularvorlagen. Die Informationen und Hinweise im Thema Security Levels, E-Mail Deployment, and Remote Form Templates sind ebenfalls wichtig.
ms.openlocfilehash: 76cc6dfdbd2c01827182c348281a98ad7cd17b69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426800"
---
# <a name="deploying-signed-infopath-form-templates"></a>Bereitstellen signierter InfoPath-Formularvorlagen

Bevor Sie dieses Thema lesen, finden Sie im Abschnitt "signierte Formularvorlagen" Weitere Informationen zur Sicherheit von signierten Formularvorlagen unter [zusätzliche InfoPath-Formular Sicherheitskonzepte](additional-infopath-form-security-concepts.md) . Die Informationen und Hinweise im Thema [Security Levels, E-Mail Deployment, and Remote Form Templates](security-levels-email-deployment-and-remote-form-templates.md) sind ebenfalls wichtig. 
  
## <a name="digitally-signing-a-form-template"></a>Digitales Signieren einer Formularvorlage

Wenn Sie eine Formularvorlage digital signieren, können Sie die Sicherheitsstufe für die Formularvorlage auf voll vertrauenswürdig festlegen, was dazu führt, dass das Formular auf Dateien und Einstellungen auf dem Computer des Benutzers oder in einer anderen Domäne zugreifen kann. (Auch die digitale Signierung einer Formularvorlage hindert Sie nicht daran, andere Sicherheitsstufen zu verwenden, wenn Sie es vorziehen. Sie legen die Sicherheitsstufe einer signierten Formularvorlage auf die Domäne oder eingeschränkte Sicherheitsstufe fest.) Darüber hinaus können Sie die signierte Formularvorlage für Benutzer bereitstellen, die ein e-Mail-Programm verwenden und dann die signierte Formularvorlage später automatisch aktualisieren, indem Sie die aktualisierte Version an die Benutzer als Anlage einer e-Mail-Nachricht senden, indem Sie die folgenden Schritte ausführen:
  
### <a name="to-digitally-sign-a-form-template"></a>So können Sie eine Formularvorlage digital signieren

1. Klicken Sie im InfoPath-Designer auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
2. Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Sicherheit und Vertrauensstellung**. 
    
3. Aktivieren Sie unter **Signatur der Formularvorlage** das Kontrollkästchen **Diese Formularvorlage signieren**. 
    
4. Klicken Sie auf **Zertifikat auswählen**.
    
5. Klicken Sie im Dialogfeld **Zertifikat auswählen** auf das Zertifikat, mit dem Sie das Formular digital signieren möchten. 
    
> [!NOTE]
> Mit der Schaltfläche **Zertifikat erstellen** im Dialogfeld **Formularoptionen** kann ein Testzertifikat zum Signieren einer Formularvorlage generiert werden. Das Testzertifikat sollte nur zu Testzwecken zum Signieren von Formularvorlagen verwendet werden. Mit Testzertifikaten sollten keine Formularvorlagen signiert werden, die öffentlich weitergegeben werden. Die Zertifikate werden nicht von einer Zertifizierungsstelle ausgestellt, deren Stammzertifikat bereits auf dem Computer eines Benutzers vertrauenswürdig ist, weshalb die Testzertifikate auf dem Computer des Benutzers nicht ordnungsgemäß überprüft werden. Wenn Sie eine mit einem Testzertifikat signierte Formularvorlage bereitstellen, können Benutzer Ihrer Formularvorlage diese höchstwahrscheinlich nicht öffnen. 
  
## <a name="establishing-a-trusted-root-certificate-and-publisher"></a>Einrichten eines vertrauenswürdigen Stammzertifikats und eines vertrauenswürdigen Herausgebers

  Das vertrauenswürdige Stammzertifikat des Zertifikats, mit dem die Formularvorlage signiert wird, muss im Speicher für vertrauenswürdige Stammzertifikate auf dem Clientcomputer vorhanden sein. Andernfalls kann der Herausgeber der Formularvorlage nicht überprüft werden, und Benutzer Ihrer Formularvorlage haben nicht die Möglichkeit, dem Herausgeber zu vertrauen. Falls sich das vertrauenswürdige Stammzertifikat im Speicher für vertrauenswürdige Stammzertifikate befindet, aber der Herausgeber nicht in der Liste vertrauenswürdiger Herausgeber vorhanden ist, werden die Benutzer aufgefordert bzw. haben die Möglichkeit, dem Herausgeber der Formularvorlage zu vertrauen. 
  
> [!NOTE]
> Wenn eine signierte Formularvorlage die Domänensicherheitsstufe oder die eingeschränkte Sicherheitsstufe erfordert, überprüft InfoPath mithilfe der Signatur, ob die Formularvorlage nach dem Signieren manipuliert wurde. Außerdem bestimmt InfoPath mithilfe der Signatur, ob die Formularvorlage automatisch aktualisiert werden kann. 
  
## <a name="deploying-signed-form-templates-with-full-trust-access"></a>Bereitstellen signierter Formularvorlagen mit der Sicherheitsstufe "Voll vertrauenswürdig"

Das primäre Szenario für die Bereitstellung signierter Formularvorlagen besteht darin, Domänen ähnliche Funktionen wie automatische Updates in voll vertrauenswürdigen Formularen zu aktivieren. Eine signierte Formularvorlage, die den Zugriff mit voller Vertrauenswürdigkeit anfordert, hat denselben Zugriff auf Systemressourcen wie ein *voll vertrauenswürdiges Formular* . Eine ausführliche Erläuterung der Funktionsweise voll vertrauenswürdiger Formulare und wie sie erstellt und bereitgestellt werden finden Sie unter [Grundlegendes zu voll vertrauenswürdigen Formularen](understanding-fully-trusted-forms.md).
  
In Abhängigkeit von der EDV-Umgebung Ihrer Organisation ziehen Sie jedoch möglicherweise die Verwendung signierter Formularvorlagen oder voll vertrauenswürdiger Formulare vor. Beispielsweise bietet die Verwendung einer signierten Formularvorlage, die die Sicherheitsstufe Voll vertrauenswürdig erfordert, anstelle eines registrierten, voll vertrauenswürdigen Formulars die folgenden Vorteile:
  
- Im Gegensatz zu einer unsignierten, voll vertrauenswürdigen Formularvorlage ist keine Registrierung erforderlich.
    
- Die automatische Aktualisierung der Formularvorlage ist möglich.
    
Da eine signierte Formularvorlage, die die Sicherheitsstufe Voll vertrauenswürdig erfordert, keine Registrierung erfordert, müssen Sie diese nicht mit einem Installer-Paket oder einer Skriptdatei bereitstellen. Dadurch wird die Bereitstellung einer voll vertrauenswürdigen Formularvorlage erheblich vereinfacht.
  
Beim Aktualisieren der signierten Formularvorlage, die die Sicherheitsstufe Voll vertrauenswürdig erfordert, können Sie einfach die aktualisierte Vorlage an den Benutzer senden oder diese in einem freigegebenen Speicherort aktualisieren. Wenn der Benutzer die aktualisierte Vorlage öffnet, wird der Benutzer nicht aufgefordert, und die ältere Kopie auf dem Computer des Benutzers wird automatisch mit der aktualisierten Version überschrieben. Falls Sie die Vorlage in einem freigegebenen Speicherort aktualisiert haben, kann der Benutzer die aktualisierte Kopie ohne Bestätigung verwenden.
  
Falls Sie ein unsigniertes, voll vertrauenswürdiges Formular aktualisieren möchten, müssen Sie das Formular erneut packen und registrieren. Darüber hinaus kann eine vorhandene und installierte voll vertrauenswürdige Formularvorlage nur für den Pfad des lokalen Computers, nicht aber für einen Netzwerkpfad verwendet werden, da für den Registrierungsvorgang ein lokaler Computerpfad nicht in einen Netzwerkpfad geändert werden kann. Da allerdings ein Zertifikat zum Signieren einer Formularvorlage erforderlich ist, sollten Sie eventuell voll vertrauenswürdige, registrierte Formularvorlagen bereitstellen, wenn Sie kein Zertifikat erwerben möchten.
  
## <a name="deploying-signed-form-templates-with-domain-or-restricted-access"></a>Bereitstellen signierter Formularvorlagen mit der Domänensicherheitsstufe oder der eingeschränkten Sicherheitsstufe 

Eine signierte Formularvorlage mit der Domänensicherheitsstufe oder der eingeschränkten Sicherheitsstufe bietet außerdem den Vorteil der automatischen Aktualisierungsfunktion. Sie können beispielsweise eine signierte Formularvorlage in einer Dokumentbibliothek auf einem Server veröffentlichen, auf dem Microsoft SharePoint Foundation ausgeführt wird, oder auf einem Server mit einer Domänen Sicherheitsstufe. Wenn Sie Ihre Formularvorlage in dem freigegebenen Speicherort aktualisieren, erhalten die Benutzer automatisch die aktualisierte Kopie.
  

