	---------------------------------------------------------------------------------------------------------------	
	-- General Info:
	-- rsPointCacheMerger.mcr
	-- Main concept and code by Albert Alomar
	-- albert.alomar@gmail.com
	-- MaxScript Template, tips and coaching by Eduardo Serna
	-- version 1.02
	-- Created On: 08/09/2011
	-- Modified On: 19/12/2011
	-- tested using Max 2012 x64
	---------------------------------------------------------------------------------------------------------------	

	---------------------------------------------------------------------------------------------------------------	
	-- Description:
	-- 1) Makes a snapshot of each selected object and merges it into a new
	--      compound mesh centered at the world origin.
	-- 2) Bakes each objects animations into PC2 files.
	-- 3) Takes each PC2 file and duplicates all the vertex-baked 
	--      movement into a new PC2 file.
	-- 4) Finally applies a PointCache2 modifier to the new compound mesh and
	--      loads the new merged file that contains all the vertex movements.
	---------------------------------------------------------------------------------------------------------------	

	---------------------------------------------------------------------------------------------------------------	
	-- To Do:
	-- Add option to merge already created PC2 files
	---------------------------------------------------------------------------------------------------------------	

	---------------------------------------------------------------------------------------------------------------	
	-- History:

	-- Betas
	-- 1.0 Initial beta private release (12/09/2011)
	-- 1.1 Quick beta patch to order alphabetically the objects when added to the selected list. (13/09/2011)

	-- Final Releases
	-- 1.00 First Public Release (05/12/2011)
	-- 1.01 Changelog: (12/12/2011)
	-- 		· Fixed the corrupted texturing of the first mesh attached
	--		· Fixed an incorrect handling of non geometry objects selection.
	--		· Added default settings to fix the first execution, when still there isn't any .ini file.
	--		· Added a selection filter to exlude a PF_Source geometry.
	--		· Added Undo option (forced garbage collection seems to be unnecessary in most cases).
	-- 1.02 Changelog: (19/12/2011)
	-- 		· Now before the execution the focus is removed from the "Modify" Panel to prevent a weird behaviour in some systems when a lot of objects are going to be attached.
	-- 		· Improved the attaching method, now does not need to convert the mesh to poly. In some meshes that could change the topology and then make the script to fail.
	---------------------------------------------------------------------------------------------------------------	

	---------------------------------------------------------------------------------------------------------------	
	-- License:
	-- Script and Source Code licensed under a Creative Commons Attribution 3.0 License
	-- Read license details here: http://creativecommons.org/licenses/by/3.0/
	--
	-- What this license means is that I give you this script for free and let you use it or 
	-- any part of its source code in your personal and comercial projects, BUT
	-- if you do you must mention me ( Albert Alomar Juan ) and my website ( www.recubo.biz ).
	---------------------------------------------------------------------------------------------------------------	