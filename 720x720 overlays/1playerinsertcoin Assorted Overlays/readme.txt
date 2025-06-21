1playerinsertcoin Assorted Overlays

All of the overlays in this folder are centered except for Perfect_GBC-720p(4x offset). I recommend using the sharp-shimmerless interpolation shader (default in muOS Pixie) for non-integer scale overlays.

Scaling Settings:

1. Integer scale overlays except Perfect_GBC-720p(4x offset)

	Main Menu > Settings > Video > Scaling

    		Integer Scale > ON

    		Integer Scale Axis > (shouldn't matter)

		Integer Scale Scaling > Underscale

    		Aspect Ratio > Core provided
         
		Viewport Anchor Bias X > 0.50
         
        	Viewport Anchor Bias Y > 0.50

    		Bilinear Filtering > OFF

    		Crop Overscan > OFF


2. Perfect_GBC-720p(4x offset)

	Main Menu > Settings > Video > Scaling

    		Integer Scale > ON

    		Integer Scale Axis > (shouldn't matter)

		Integer Scale Scaling > Underscale

    		Aspect Ratio > Custom
         
		Custom Aspect Ratio (X Position) > 0

		Custom Aspect Ratio (Y Position) > 41

		Custom Aspect Ratio (Width) > 640 (4x)

		Custom Aspect Ratio (Height) > 576 (4x)

		Viewport Anchor Bias X > 0.50
         
        	Viewport Anchor Bias Y > 0.00

    		Bilinear Filtering > OFF

    		Crop Overscan > OFF
	

3. Non-integer scale overlays

	Main Menu > Settings > Video > Scaling

    		Integer Scale > OFF

    		Integer Scale Axis > (shouldn't matter)

		Integer Scale Scaling > (shouldn't matter)

    		Aspect Ratio > Core Provided or 4:3 for Perfect_GG-720p(4x3)
         
		Viewport Anchor Bias X > 0.50
         
        	Viewport Anchor Bias Y > 0.50

    		Bilinear Filtering > OFF

    		Crop Overscan > OFF