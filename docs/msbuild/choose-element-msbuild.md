---
title: "Choose 元素 (MSBuild) | Microsoft Docs"
ms.custom: 
ms.date: 03/13/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: http://schemas.microsoft.com/developer/msbuild/2003#Choose
dev_langs:
- VB
- CSharp
- C++
- jsharp
- xml
helpviewer_keywords:
- <Choose> Element [MSBuild]
- Choose Element [MSBuild]
ms.assetid: 7b8b025a-d944-4f5c-9018-c89fc2ef146d
caps.latest.revision: "8"
author: kempb
ms.author: kempb
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: 38ddfed161e04948eb3725192c95025dec5c473b
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="choose-element-msbuild"></a>Choose 元素 (MSBuild)
评估子元素，选择一组 `ItemGroup` 元素和/或 `PropertyGroup` 元素进行评估。  

 \<Project>  
 \<Choose>  
 \<When>  
 \<Choose>  
 ...  
 \<Otherwise>  
 \<Choose>  
 ...  

## <a name="syntax"></a>语法  

```  
<Choose>  
    <When Condition="'StringA'=='StringB'">... </When>  
    <Otherwise>... </Otherwise>  
</Choose>  
```  

## <a name="attributes-and-elements"></a>特性和元素  
 下列各节描述了特性、子元素和父元素。  

### <a name="attributes"></a>特性  
 无。  

### <a name="child-elements"></a>子元素  

|元素|描述|  
|-------------|-----------------|  
|[Otherwise](../msbuild/otherwise-element-msbuild.md)|可选元素。<br /><br /> 当所有 `When` 元素的条件的计算结果为 `false` 时，指定要计算的代码块 `PropertyGroup` 和 `ItemGroup` 元素。 `Choose` 元素中可能没有或只有一个 `Otherwise` 元素，并且它必须是最后一个元素。|  
|[When](../msbuild/when-element-msbuild.md)|必需的元素。<br /><br /> 指定一个可能的代码块供 `Choose` 元素选择。 `Choose` 元素中可能有一个或多个 `When` 元素。|  

### <a name="parent-elements"></a>父元素  

|元素|描述|  
|-------------|-----------------|  
|[Otherwise](../msbuild/otherwise-element-msbuild.md)|当所有 `When` 元素的条件的计算结果为 `false` 时，指定要执行的代码块。|  
|[Project](../msbuild/project-element-msbuild.md)|[!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] 项目文件必需的根元素。|  
|[When](../msbuild/when-element-msbuild.md)|指定一个可能的代码块供 `Choose` 元素选择。|  

## <a name="remarks"></a>备注  
 `Choose`、`When` 和 `Otherwise` 元素一起用来提供一种方式，通过这种方式选择代码的一部分来执行许多种可能的替代选择。 有关详细信息，请参阅[条件构造](../msbuild/msbuild-conditional-constructs.md)。  

## <a name="example"></a>示例  
 以下项目使用 `Choose` 元素来选择要在 `When` 元素中设置的属性值组。 如果两个 `When` 元素的 `Condition` 属性的计算结果均为 `false`，则将设置 `Otherwise` 元素中的属性值。  

```xml  
<Project  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003" >  
    <PropertyGroup>  
        <Configuration Condition="'$(Configuration)' == ''">Debug</Configuration>  
        <OutputType>Exe</OutputType>  
        <RootNamespace>ConsoleApplication1</RootNamespace>  
        <AssemblyName>ConsoleApplication1</AssemblyName>  
        <WarningLevel>4</WarningLevel>  
    </PropertyGroup>  
    <Choose>  
        <When Condition=" '$(Configuration)'=='debug' ">  
            <PropertyGroup>  
                <DebugSymbols>true</DebugSymbols>  
                <DebugType>full</DebugType>  
                <Optimize>false</Optimize>  
                <OutputPath>.\bin\Debug\</OutputPath>  
                <DefineConstants>DEBUG;TRACE</DefineConstants>  
            </PropertyGroup>  
            <ItemGroup>  
                <Compile Include="UnitTesting\*.cs" />  
                <Reference Include="NUnit.dll" />  
            </ItemGroup>  
        </When>  
        <When Condition=" '$(Configuration)'=='retail' ">  
            <PropertyGroup>  
                <DebugSymbols>false</DebugSymbols>  
                <Optimize>true</Optimize>  
                <OutputPath>.\bin\Release\</OutputPath>  
                <DefineConstants>TRACE</DefineConstants>  
            </PropertyGroup>  
        </When>  
        <Otherwise>  
            <PropertyGroup>  
                <DebugSymbols>true</DebugSymbols>  
                <Optimize>false</Optimize>  
                <OutputPath>.\bin\$(Configuration)\</OutputPath>  
                <DefineConstants>DEBUG;TRACE</DefineConstants>  
            </PropertyGroup>  
        </Otherwise>  
    </Choose>  
    <Import Project="$(MSBuildBinPath)\Microsoft.CSharp.targets" />  
</Project>  
```  

## <a name="see-also"></a>请参阅  
 [条件构造](../msbuild/msbuild-conditional-constructs.md)   
 [项目文件架构参考](../msbuild/msbuild-project-file-schema-reference.md)
